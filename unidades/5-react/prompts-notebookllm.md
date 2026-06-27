# Unidade 5 — Promontos para NotebookLM

> Carregue como fontes:
> - `docs/react.md`
> - `unidades/5-react/conteudo.md`
> - `exercicios.md` (exercícios 5.1 e 5.2)

---

## Prompt 1 — Guia de estudo da unidade

```
Crie um guia de estudo da Unidade 5 (ReAct). Organize em:
- Definição (1 linha)
- Origem acadêmica (paper, ano, arXiv ID)
- Por que ReAct supera CoT puro e Acting puro (com tabela)
- Como funciona (trajetória Thought/Action/Observation)
- Resultados empíricos (HotpotQA, Fever, ALFWorld, WebShop)
- Quando usar (3 casos) e limitações (3)
- 2 dicas práticas
```

---

## Prompt 2 — Quiz de 10 questões

```
Gere 10 questões de múltipla escolha (4 alternativas) sobre ReAct:
- 2 sobre definição e origem (paper, ano, arXiv)
- 2 sobre a trajetória Thought/Action/Observation
- 2 sobre CoT vs Acting vs ReAct
- 2 sobre resultados empíricos (benchmarks)
- 2 sobre limitações documentadas
Marque a resposta correta e justifique em 1 linha citando a seção.
```

---

## Prompt 3 — Flashcards

```
Gere 12 flashcards "Frente: pergunta / Verso: resposta (máx 15 palavras)":
- 2 cards: o que é ReAct + origem (Yao 2022, arXiv:2210.03629)
- 3 cards: Thought / Action / Observation
- 2 cards: CoT vs ReAct / Acting vs ReAct
- 2 cards: resultados empíricos (HotpotQA, Fever)
- 2 cards: limitações (dependência de buscas, recuperação limitada)
- 1 card: ReAct vs React (web framework)
```

---

## Prompt 4 — Podcast (Audio Overview) da unidade

```
Crie um diálogo de podcast (2 apresentadores, ~8 min) sobre ReAct.
Estrutura:
1. O diferencial desta unidade: primeira técnica com paper acadêmico
2. Por que CoT puro falha (alucina fatos) e Acting puro falha (não raciocina)
3. A trajetória Thought/Action/Observation, com o exemplo do Colorado orogeny
4. Resultados empíricos: ReAct supera Acting em todos, empatou com CoT em alguns
5. Limitações honestas: depende da qualidade das buscas
6. Implementação: LangChain usa ReAct por padrão
Tom didático. Termine com: "Na próxima unidade: BDI, modelo de agentes que inspirou ReAct."
```

---

## Prompt 5 — Construção guiada de trajetória ReAct

```
Vou fazer uma pergunta que exige informação externa. Escreva a trajetória
ReAct esperada (Thought/Action/Observation), em 3-5 passos, sem executar
de fato — apenas planeje. Cada Thought deve justificar o próximo Action.
Cada Action deve chamar uma ferramenta de busca. A resposta final deve
integrar todas as observações.
Pergunta: [escreva sua pergunta aqui]
```

---

## Prompt 6 — Análise de trajetória ReAct

```
[Após colar uma trajetória Thought/Action/Observation que você escreveu]
Avalie esta trajetória verificando:
1. Cada Thought justifica o próximo Action? (sim/não + por quê)
2. Cada Action chama uma ferramenta de busca? (sim/não)
3. As Observations são consistentes com os Actions? (sim/não)
4. A resposta final integra as observações? (sim/não)
5. Há passo desnecessário ou faltando? (qual)
Formato: tabela + 2 sugestões de melhoria.
```

---

## Prompt 7 — Comparação CoT vs ReAct vs BDI

```
Crie uma tabela comparando CoT (Wei 2022), ReAct (Yao 2022) e BDI
(Bratman 1987; Rao & Georgeff 1995). Colunas: origem, domínio, acesso
externo, raciocínio explícito, estado interno, formalização lógica.
Por fim, escreva 2 linhas explicando como ReAct "ressuscita" a ideia
clássica de raciocínio + ação que o BDI formalizou teoricamente antes.
```

---

## Prompt 8 — Quando NÃO usar ReAct

```
Liste 5 situações em que ReAct é inadequado ou desnecessário. Para cada:
1. Por que ReAct falha ou é over-engineering nesta situação
2. O que usar no lugar (CoT puro, RACE, TAG, etc.)
3. Justificativa em 1 linha
```

---

## Prompt 9 — FAQ da unidade

```
Gere um FAQ com 8 perguntas que um aluno faria sobre ReAct:
- "ReAct tem a ver com React (JavaScript)?"
- "ReAct é científico?"
- "Preciso programar para usar ReAct?"
- "CoT não basta?"
- "ReAct funciona em qualquer LLM?"
- "Como implemento ReAct na prática?"
- "ReAct alucina?"
- "ReAct vs BDI, qual usar?"
Respostas em até 3 linhas.
```

---

## Prompt 10 — Síntese para revisão

```
Resuma a Unidade 5 em uma página A4 organizada em:
- Título: "ReAct — Reasoning + Acting (Yao et al., 2022)"
- Caixa destaque: "Primeira técnica do curso com paper peer-reviewed"
- Diagrama da trajetória Thought→Action→Observation→...→Finish
- Tabela CoT vs Acting vs ReAct
- Tabela resultados empíricos (4 benchmarks)
- Tabela quando usar / limitações
- Caixa com código LangChain (5 linhas)
Formato pronto para imprimir como PDF.
```

---

## Dica de uso

Carregue **apenas** os 3 arquivos listados no topo. Para comparação com CoT e BDI (prompt 7), adicione `docs/bdi.md` e `docs/prompt-engineering.md` temporariamente.