# Unidade 5 — ReAct: raciocínio + ação

> Curso: Prompt Engineering na Prática
> Materiais: vídeo (10-12 min) + apresentação + infográfico
> Carga horária: 2h (vídeo + leitura + 2 exercícios)

---

## 1. Objetivos de aprendizagem

Ao final desta unidade, o aluno será capaz de:

1. **Definir** o framework ReAct (Reasoning + Acting) e sua origem acadêmica.
2. **Explicar** por que ReAct supera CoT puro e Acting puro.
3. **Escrever** trajetórias Thought/Action/Observation para tarefas que exigem informação externa.
4. **Reconhecer** as limitações empíricas documentadas no paper.

---

## 2. Conteúdo

### 2.1 Definição

O **ReAct** é um framework introduzido por **Yao et al. (2022)** no qual Modelos de Linguagem de Grande Porte (LLMs) são usados para gerar, de forma intercalada, **trilhas de raciocínio** (*reasoning traces*) e **ações específicas da tarefa** (*task-specific actions*).

> **Nome:** *ReAct* = **Re**asoning + **Act**ing (não confundir com o framework web React).

### 2.2 Origem acadêmica (diferencial desta unidade)

Diferente de RACE/TAG/CARE (heurísticas práticas sem paper), o ReAct tem:
- **Paper acadêmico peer-reviewed:** Yao et al., 2022, arXiv:2210.03629
- **Resultados empíricos em benchmarks públicos:** HotpotQA, Fever, ALFWorld, WebShop
- **Implementação em bibliotecas de mercado:** LangChain

### 2.3 Motivação

| Abordagem | Limite |
|-----------|--------|
| **Chain-of-Thought (CoT)** | Permite raciocinar, mas **sem acesso ao mundo externo** — pode alucinar fatos e propagar erros. |
| **Acting puro** | Permite agir/buscar, mas **sem raciocínio explícito** — falha em decompor metas em submetas. |

O ReAct **combina as duas forças**: raciocínio para planejar e guiar buscas; ação para obter evidências externas que fundamentem o raciocínio.

### 2.4 Como funciona

A trajetória é composta por passos intercalados:

```
Thought N:  (raciocínio sobre o próximo passo)
Action N:   Tool[input]              (chamada a ferramenta/ambiente)
Observation N: (resultado retornado pela ferramenta)
...
Thought M:  (síntese final)
Action M:   Finish[resposta final]
```

- **Thought** — reflexão livre do modelo: decompor a pergunta, extrair informação, raciocinar aritmeticamente, formular busca, sintetizar resposta.
- **Action** — chamada a uma ferramenta externa (`Search[...]`, `Lookup[...]`, `Calculator[...]`, `Finish[...]`).
- **Observation** — resultado retornado pelo ambiente/ferramenta.

> A ideia central: **o raciocínio orienta o que buscar; a busca fornece evidências que sustentam o raciocínio**.

### 2.5 Exemplo (adaptado de Yao et al., 2022)

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

### 2.6 Resultados empíricos (Yao et al., 2022)

#### Tarefas conhecimento-intensivas (HotpotQA, Fever, com PaLM-540B)
- **ReAct supera "Act puro"** em ambas — raciocinar melhora o uso das ações.
- **ReAct × CoT:** ReAct supera CoT em *Fever*; fica atrás em *HotpotQA*.
  - **CoT** sofre de **alucinação factual** quando não tem acesso externo.
  - **ReAct** tem flexibilidade menor na formulação dos passos e depende muito da qualidade da busca.

**Conclusão dos autores:** a melhor abordagem combina **ReAct + CoT + Self-Consistency**.

#### Tarefas de tomada de decisão (ALFWorld, WebShop)
- ReAct supera "Act puro" em ambos.
- Sem *Thoughts*, o agente falha em decompor metas em submetas.
- Ainda assim, métodos baseados em prompt **ficam aquém do desempenho humano**.

### 2.7 Quando usar ReAct

- Tarefas que exigem **informação externa** (busca web, base de conhecimento, APIs).
- **Tomada de decisão multi-etapas** com dependência entre passos.
- Quando importa **auditabilidade/interpretabilidade** — a trilha *Thought→Action→Observation* torna o raciocínio explícito.
- Agentes que precisam **se recuperar de erros** durante a execução.

### 2.8 Limitações

- **Dependência da qualidade das ferramentas externas** — buscas pouco informativas descarrilam o raciocínio.
- **Restrição estrutural** — o formato *Thought/Action/Observation* reduz flexibilidade na formulação de passos.
- **Recuperação limitada** — após um erro causado por observação ruim, é difícil recuperar e reformular o pensamento.
- Ainda **abaixo do desempenho humano** em tarefas complexas de decisão.

### 2.9 Implementação prática (LangChain)

ReAct é o padrão de agente em bibliotecas como LangChain:

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

Trajetória gerada:

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

### 2.10 Comparação: ReAct × CoT × BDI

| Dimensão | ReAct | Chain-of-Thought (CoT) | BDI |
|---|---|---|---|
| Origem | Yao et al., 2022 | Wei et al., 2022 | Bratman 1987; Rao & Georgeff 1995 |
| Domínio | Prompting para LLMs | Prompting para LLMs | Arquitetura de agentes de software |
| Acesso externo | ✅ Sim (tools) | ❌ Não | ✅ Via sensores/events |
| Raciocínio explícito | ✅ *Thoughts* | ✅ Passos de raciocínio | ✅ Deliberação |
| Estado interno estruturado | Implícito | Implícito | ✅ Beliefs/Desires/Intentions |
| Formalização lógica | Não | Não | ✅ BDICTL, LORA |

> **ReAct** é uma **técnica de prompt** que ressuscita, na prática, a ideia clássica de **raciocínio + ação** que o BDI formalizou teoricamente décadas antes.

---

## 3. Exercícios da unidade

### Exercício 5.1 — Trajetória ReAct para pergunta do Python (guiado)
Escreva a trajetória Thought/Action/Observation para: *"Qual o PIB per capita do país onde nasceu o criador da linguagem Python?"*. **Gabarito no `exercicios.md`.**

### Exercício 5.2 — Pergunta com 3+ buscas (livre)
Crie uma pergunta que exija 3+ buscas externas encadeadas e escreva a trajetória Thought/Action/Observation esperada. Tema livre.

---

## 4. Leitura complementar

- `docs/react.md` — documento base completo com todos os exemplos, resultados empíricos e referências

---

## 5. Fontes verificadas

1. **Yao, S. et al.** (2022). *ReAct: Synergizing Reasoning and Acting in Language Models*. arXiv:2210.03629. https://arxiv.org/abs/2210.03629
2. **Wei, J. et al.** (2022). *Chain-of-Thought Prompting Elicits Reasoning in Large Language Models*. arXiv:2201.11903. https://arxiv.org/abs/2201.11903
3. **Prompt Engineering Guide (DAIR.AI)** — ReAct: https://www.promptingguide.ai/techniques/react
4. **LangChain** — ReAct agent types: https://python.langchain.com/docs/modules/agents/agent_types/react

### Benchmarks citados
5. **HotpotQA** — https://hotpotqa.github.io/
6. **Fever** — https://fever.ai/
7. **ALFWorld** — https://alfworld.github.io/
8. **WebShop** — https://webshop-pnlp.github.io/

> **Transparência:** ReAct é técnica **documentada por paper acadêmico peer-reviewed** e reconhecida por todas as fontes autoritativas. Primeira técnica do curso com embasamento científico formal.