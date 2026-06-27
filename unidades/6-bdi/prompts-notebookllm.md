# Unidade 6 — Promontos para NotebookLM

> Carregue como fontes:
> - `docs/bdi.md`
> - `unidades/6-bdi/conteudo.md`
> - `exercicios.md` (exercícios 6.1 e 6.2)

---

## Prompt 1 — Guia de estudo da unidade

```
Crie um guia de estudo da Unidade 6 (BDI). Organize em:
- Definição (1 linha)
- Aviso importante: BDI NÃO é framework de prompt
- Origem acadêmica (Bratman 1987, Rao & Georgeff 1995)
- Os 3 componentes (B, D, I) + componentes adicionais (Belief set, Goals, Plans, Events)
- Ciclo do interpretador BDI (7 passos)
- Analogia a prompts (como usar B/D/I em prompts)
- Quando usar a analogia (3 casos) e limitações (3)
```

---

## Prompt 2 — Quiz de 10 questões

```
Gere 10 questões de múltipla escolha (4 alternativas) sobre BDI:
- 2 sobre definição e origem (Bratman, Rao & Georgeff)
- 2 sobre os 3 componentes (B, D, I)
- 2 sobre o ciclo do interpretador (7 passos)
- 2 sobre a analogia a prompts (e o aviso de que NÃO é framework de prompt)
- 2 sobre pegadinhas (ex.: "BDI é framework de prompt?", "Beliefs = conhecimento?")
Marque a resposta correta e justifique em 1 linha.
```

---

## Prompt 3 — Flashcards

```
Gere 12 flashcards "Frente: pergunta / Verso: resposta (máx 15 palavras)":
- 3 cards: o que significa B, D, I
- 2 cards: origem (Bratman 1987, Rao & Georgeff 1995)
- 2 cards: ciclo interpretador (7 passos resumidos)
- 2 cards: quando usar / quando não usar a analogia
- 2 cards: pegadinhas (BDI ≠ framework de prompt, Beliefs ≠ conhecimento)
- 1 card: BDI vs ReAct
```

---

## Prompt 4 — Podcast (Audio Overview) da unidade

```
Crie um diálogo de podcast (2 apresentadores, ~8 min) sobre BDI.
Estrutura:
1. Aviso: BDI não é framework de prompt — é modelo de agentes
2. Origem acadêmica: Bratman 1987 (filosofia) + Rao & Georgeff 1995 (IA)
3. Os 3 componentes: Beliefs, Desires, Intentions
4. O ciclo do interpretador (perceive → deliberate → intend → execute)
5. A analogia para prompts: como usar B/D/I num prompt
6. O exemplo do planejador financeiro (dívida vs investimento)
7. Por que BDI é a técnica com embasamento mais robusto do curso
Tom didático. Termine com: "Na próxima unidade: rúbricas, para avaliar tudo isso."
```

---

## Prompt 5 — Construção guiada de prompt BDI

```
Vou descrever uma tarefa que precisa de um "agente com estado interno".
Construa um prompt no formato BDI (analogia):
- Beliefs: fatos do domínio + regras + dados do caso
- Desires: objetivos que o agente deve perseguir
- Intentions: passos concretos numerados
Para cada componente, explique por que escolheu esse conteúdo.
Tarefa: [descreva sua tarefa aqui]
```

---

## Prompt 6 — Crítica de prompt BDI

```
[Após colar um prompt BDI que você escreveu] Avalie este prompt verificando:
1. Beliefs contém fatos do domínio E regras (não só opiniões)?
2. Desires são objetivos (não ações)?
3. Intentions são passos concretos e numerados (não vagos)?
4. A separação Beliefs/Desires/Intentions é clara?
5. Esta tarefa realmente precisa de BDI, ou RACE/CARE bastariam?
Formato: tabela + 2 sugestões de melhoria.
```

---

## Prompt 7 — Comparação ReAct vs BDI

```
Compare ReAct (Unidade 5) e BDI (Unidade 6) em uma tabela única.
Colunas: origem, domínio, acesso externo, raciocínio explícito, estado
interno estruturado, formalização lógica, quando usar em prompts.
Escreva 2 linhas explicando como ReAct "ressuscita" na prática a ideia
clássica de raciocínio + ação que o BDI formalizou teoricamente antes.
```

---

## Prompt 8 — Quando NÃO usar BDI em prompts

```
Liste 5 situações em que usar BDI como analogia para prompts é
over-engineering. Para cada:
1. Por que BDI é exagero nesta situação
2. O que usar no lugar (RACE, TAG, CARE, ReAct)
3. Justificativa em 1 linha
```

---

## Prompt 9 — FAQ da unidade

```
Gere um FAQ com 8 perguntas que um aluno faria sobre BDI:
- "BDI é framework de prompt?"
- "Preciso programar para usar BDI?"
- "Beliefs é o mesmo que contexto?"
- "BDI é científico?"
- "Onde BDI é usado na prática?"
- "BDI vs ReAct, qual a diferença?"
- "Posso usar BDI com RACE?"
- "Por que BDI tem lógica modal?"
Respostas em até 3 linhas.
```

---

## Prompt 10 — Síntese para revisão

```
Resuma a Unidade 6 em uma página A4 organizada em:
- Título: "BDI — Belief, Desire, Intention (Bratman 1987; Rao & Georgeff 1995)"
- Caixa destaque: "BDI NÃO é framework de prompt — é modelo de agentes"
- Diagrama dos 3 componentes + componentes adicionais
- Ciclo do interpretador (7 passos em diagrama)
- Caixa "Analogia a prompts: Beliefs/Desires/Intentions"
- Tabela quando usar / quando não usar
- Comparação ReAct vs BDI (1 linha)
Formato pronto para imprimir como PDF.
```

---

## Dica de uso

Carregue **apenas** os 3 arquivos listados no topo. Para comparação ReAct vs BDI (prompt 7), adicione `docs/react.md` e `unidades/5-react/conteudo.md` temporariamente.