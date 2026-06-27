# ReAct — Reasoning + Acting

> Framework de prompt para LLMs que combina raciocínio e ação.
> Documentação de apoio para cursos online.

---

## 1. Definição

O **ReAct** é um framework introduzido por **Yao et al. (2022)** no qual Modelos de Linguagem de Grande Porte (LLMs) são usados para gerar, de forma intercalada, **trilhas de raciocínio** (*reasoning traces*) e **ações específicas da tarefa** (*task-specific actions*).

Gerar trilhas de raciocínio permite ao modelo:
- **induzir, acompanhar e atualizar planos de ação**;
- **lidar com exceções**.

A etapa de ação permite **interagir com fontes externas** — como bases de conhecimento ou ambientes — para coletar informações adicionais, levando a respostas **mais confiáveis e factuais**.

> **Nome:** *ReAct* = **Re**asoning + **Act**ing (não confundir com o framework web React).

---

## 2. Motivação

Antes do ReAct, duas abordagens dominavam:

| Abordagem | Limite |
|-----------|--------|
| **Chain-of-Thought (CoT)** | Permite raciocinar, mas **sem acesso ao mundo externo** — pode alucinar fatos e propagar erros. |
| **Acting puro** | Permite agir/buscar, mas **sem raciocínio explícito** — falha em decompor metas em submetas. |

O ReAct **combina as duas forças**: raciocínio para planejar e guiar buscas; ação para obter evidências externas que fundamentem o raciocínio.

---

## 3. Como funciona

O ReAct é inspirado na sinergia humana entre "agir" e "raciocinar" para aprender tarefas novas e tomar decisões.

Em uma execução ReAct típica, o modelo gera uma **trajetória de resolução** composta por passos intercalados:

```
Thought N:  (raciocínio sobre o próximo passo)
Action N:   Tool[input]              (chamada a ferramenta/ambiente)
Observation N: (resultado retornado pela ferramenta)
...
Thought M:  (síntese final)
Action M:   Finish[resposta final]
```

- **Thought** — reflexão livre do modelo: decompor a pergunta, extrair informação, raciocinar aritmeticamente, formular busca, sintetizar resposta.
- **Action** — chamada a uma ferramenta externa (e.g., `Search[...]`, `Lookup[...]`, `Calculator[...]`, `Finish[...]`).
- **Observation** — resultado retornado pelo ambiente/ferramenta.

A ideia central: **o raciocínio orienta o que buscar; a busca fornece evidências que sustentam o raciocínio**.

---

## 4. Exemplo (adaptado de Yao et al., 2022)

**Pergunta:** *Que altitude é encontrada na área para a qual o setor leste da orogenia do Colorado se estende?*

```
Thought 1  Preciso buscar "Colorado orogeny", encontrar a área do setor
           leste e depois a faixa de altitude dessa área.
Action 1   Search[Colorado orogeny]
Observation 1  A orogenia do Colorado foi um episódio de formação de
                montanhas no Colorado e áreas vizinhas.

Thought 2  Não menciona setor leste. Preciso buscar "eastern sector".
Action 2   Lookup[eastern sector]
Observation 2  O setor leste se estende até as High Plains...

Thought 3  Preciso buscar "High Plains" e encontrar a altitude.
Action 3   Search[High Plains]
Observation 3  High Plains: sub-região das Great Plains, altitude de
                1.800 a 7.000 ft.

Thought 4  Altitude de 1.800 a 7.000 ft — esta é a resposta.
Action 4   Finish[1.800 to 7.000 ft]
```

---

## 5. Resultados empíricos (Yao et al., 2022)

### 5.1 Tarefas conhecimento-intensivas
Avaliado em **HotpotQA** (perguntas) e **Fever** (verificação de fatos), com base PaLM-540B:

- **ReAct supera "Act puro"** em ambas — raciocinar melhora o uso das ações.
- **ReAct × CoT:** ReAct supera CoT em *Fever*; fica atrás em *HotpotQA*.
  - **CoT** sofre de **alucinação factual** quando não tem acesso externo.
  - **ReAct** tem flexibilidade menor na formulação dos passos (restrição estrutural) e depende muito da qualidade da busca — resultados não informativos descarrilam o raciocínio.

**Conclusão dos autores:** a melhor abordagem combina **ReAct + CoT + Self-Consistency**, permitindo alternar entre conhecimento interno e evidência externa.

### 5.2 Tarefas de tomada de decisão
Avaliado em **ALFWorld** (jogo em texto) e **WebShop** (ambiente de e-commerce):

- ReAct supera "Act puro" em ambos.
- Sem *Thoughts*, o agente falha em decompor metas em submetas.
- Ainda assim, métodos baseados em prompt **ficam aquém do desempenho humano** nesses ambientes.

---

## 6. Quando usar ReAct

- Tarefas que exigem **informação externa** (busca web, base de conhecimento, APIs).
- **Tomada de decisão multi-etapas** com dependência entre passos.
- Quando importa **auditabilidade/interpretabilidade** — a trilha *Thought→Action→Observation* torna o raciocínio explícito.
- Agentes que precisam **se recuperar de erros** durante a execução.

---

## 7. Limitações

- **Dependência da qualidade das ferramentas externas** — buscas pouco informativas descarrilam o raciocínio.
- **Restrição estrutural** — o formato *Thought/Action/Observation* reduz flexibilidade na formulação de passos.
- **Recuperação limitada** — após um erro causado por observação ruim, é difícil recuperar e reformular o pensamento.
- Ainda **abaixo do desempenho humano** em tarefas complexas de decisão (ALFWorld, WebShop).

---

## 8. Implementação prática (LangChain)

O ReAct é o padrão de agente implementado em bibliotecas como **LangChain**. Exemplo de uso:

```python
from langchain.agents import load_tools, initialize_agent
from langchain.llms import OpenAI

llm = OpenAI(temperature=0)
tools = load_tools(["google-serper", "llm-math"], llm=llm)

# zero-shot-react-description = agente ReAct padrão
agent = initialize_agent(
    tools, llm,
    agent="zero-shot-react-description",
    verbose=True
)

agent.run("Quem é o namorado de Olivia Wilde? "
          "Qual a idade dele elevada à 0.23?")
```

Trajetória gerada pelo agente:

```
Thought: Preciso descobrir o namorado de Olivia Wilde e calcular idade^0.23.
Action: Search["Olivia Wilde boyfriend"]
Observation: Olivia Wilde namora Harry Styles...
Thought: Preciso da idade de Harry Styles.
Action: Search["Harry Styles age"]
Observation: 29 anos
Thought: Preciso calcular 29^0.23.
Action: Calculator[29^0.23]
Observation: 2.169459462491557
Thought: Sei a resposta final.
Action: Finish[Harry Styles, 29 anos; 29^0.23 ≈ 2.17]
```

---

## 9. Comparação: ReAct × CoT × BDI

| Dimensão | ReAct | Chain-of-Thought (CoT) | BDI |
|---|---|---|---|
| Origem | Yao et al., 2022 | Wei et al., 2022 | Bratman 1987; Rao & Georgeff 1995 |
| Domínio | Prompting para LLMs | Prompting para LLMs | Arquitetura de agentes de software |
| Acesso externo | ✅ Sim (tools) | ❌ Não | ✅ Via sensores/events |
| Raciocínio explícito | ✅ *Thoughts* | ✅ Passos de raciocínio | ✅ Deliberação |
| Estado interno estruturado | Implícito | Implícito | ✅ Beliefs/Desires/Intentions |
| Formalização lógica | Não | Não | ✅ BDICTL, LORA |

> **ReAct** é uma **técnica de prompt** que ressuscita, na prática, a ideia clássica de **raciocínio + ação** que o BDI formalizou teoricamente décadas antes para agentes de software.

---

## 10. Referências (verificadas)

### Paper seminal
1. **Yao, S., Zhao, J., Yu, D., Du, N., Shafran, I., Narasimhan, K., & Cao, Y.** (2022). *ReAct: Synergizing Reasoning and Acting in Language Models*. arXiv:2210.03629. https://arxiv.org/abs/2210.03629

### CoT (referência complementar citada)
2. **Wei, J., Wang, X., Schuurmans, D., Bosma, M., Xia, F., Chi, E., Le, Q. V., & Zhou, D.** (2022). *Chain-of-Thought Prompting Elicits Reasoning in Large Language Models*. arXiv:2201.11903. https://arxiv.org/abs/2201.11903

### Documentação de referência (verificada)
3. **Prompt Engineering Guide (DAIR.AI)** — ReAct Prompting: https://www.promptingguide.ai/techniques/react
4. **LangChain** — ReAct agent types: https://python.langchain.com/docs/modules/agents/agent_types/react

### Benchmarks citados
5. **HotpotQA** — https://hotpotqa.github.io/
6. **Fever** — https://fever.ai/
7. **ALFWorld** — https://alfworld.github.io/
8. **WebShop** — https://webshop-pnlp.github.io/

---

## 11. Observação metodológica

O ReAct é uma técnica **documentada por paper acadêmico peer-reviewed** (arXiv:2210.03629, 2022) e **reconhecida por todas as fontes autoritativas** de prompt engineering consultadas (Prompt Engineering Guide / DAIR.AI, Learn Prompting, documentações de LangChain). Diferentemente de *frameworks mnemônicos* sem base acadêmica, o ReAct tem **embasamento empírico publicável**: resultados em benchmarks públicos (HotpotQA, Fever, ALFWorld, WebShop) e reprodução em bibliotecas de mercado.