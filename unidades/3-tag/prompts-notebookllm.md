# Unidade 3 — Promontos para NotebookLM

> Carregue como fontes:
> - `docs/tag.md`
> - `unidades/3-tag/conteudo.md`
> - `exercicios.md` (exercícios 3.1 e 3.2)
> - Para comparação RACE vs TAG: adicione `docs/race.md`

---

## Prompt 1 — Guia de estudo da unidade

```
Crie um guia de estudo da Unidade 3 (Framework TAG). Organize em:
- Definição (1 linha)
- Os 3 componentes em 1 parágrafo cada (T, A, G)
- A diferença crítica Task vs Action (com exemplo)
- Quando usar (3 casos) e quando NÃO usar (3 casos)
- Por que Goal é o componente mais pulado e por que não deve ser pulado
- 2 dicas práticas
```

---

## Prompt 2 — Quiz de 8 questões

```
Gere 8 questões de múltipla escolha (4 alternativas) sobre TAG:
- 2 sobre o significado de cada letra
- 2 sobre a diferença Task vs Action (foco da unidade)
- 2 sobre quando usar vs quando NÃO usar
- 2 sobre pegadinhas (ex.: "Goal opcional?", "TAG serve para código?")
Marque a resposta correta e justifique em 1 linha.
```

---

## Prompt 3 — Flashcards

```
Gere 10 flashcards "Frente: pergunta / Verso: resposta (máx 15 palavras)":
- 3 cards: o que significa T, A, G
- 2 cards: Task vs Action (a confusão mais comum)
- 2 cards: quando usar / quando não usar
- 1 card: por que Goal não pode ser pulado
- 2 cards: TAG vs RACE / TAG vs APE
```

---

## Prompt 4 — Podcast (Audio Overview) da unidade

```
Crie um diálogo de podcast (2 apresentadores, ~6 min) sobre TAG.
Estrutura:
1. Por que às vezes menos é mais (over-engineering com RACE)
2. Os 3 componentes, com o exemplo dos subject lines de reengajamento
3. A pegadinha Task vs Action — explique a diferença com exemplo
4. Por que Goal é o componente mais pulado (e por que não deveria ser)
5. Quando TAG não serve (ponte para CARE)
Tom didático. Termine com: "Na próxima unidade: CARE, com contexto rico e exemplo."
```

---

## Prompt 5 — Construção guiada de prompt TAG

```
Vou descrever uma tarefa. Construa um prompt TAG completo para ela.
Diferencie claramente Task (escopo, alto nível) e Action (método, verbo
específico). Explique brevemente por que separou assim. Ao final, dê
1 alternativa de melhoria.
Tarefa: [descreva sua tarefa aqui]
```

---

## Prompt 6 — Conversão RACE → TAG

```
[Após colar um prompt RACE que você escreveu] Converta este prompt RACE
em um prompt TAG equivalente, mantendo apenas o essencial. Liste:
1. O que foi mantido e por quê
2. O que foi descartado e por quê
3. Em qual caso o prompt TAG seria melhor que o RACE original
4. Em qual caso o RACE seria melhor que o TAG
```

---

## Prompt 7 — Tabela de decisão RACE vs TAG

```
Crie uma tabela de decisão única para escolher entre RACE e TAG.
Linhas: características da tarefa (simples, complexa, contexto evidente,
precisa de persona, multi-etapas, etc.).
Colunas: RACE recomendado? / TAG recomendado? / Por quê.
Baseie-se nos prós e contras de cada framework.
```

---

## Prompt 8 — Quando NÃO usar TAG

```
Liste 5 situações em que TAG é inadequado. Para cada uma:
1. Por que TAG falha nesta situação
2. Qual framework usar no lugar (RACE, CARE, ReAct ou BDI)
3. Justificativa em 1 linha
```

---

## Prompt 9 — FAQ da unidade

```
Gere um FAQ com 6 perguntas que um aluno faria sobre TAG:
- "Task não é a mesma coisa que Action?"
- "Goal é opcional?"
- "TAG serve para código?"
- "TAG é mais rápido que RACE, então é sempre melhor?"
- "Posso adicionar Role no TAG?"
- "TAG é científico?"
Respostas em até 3 linhas.
```

---

## Prompt 10 — Síntese para revisão

```
Resuma a Unidade 3 em uma página A4 organizada em:
- Título: "Framework TAG — Task, Action, Goal"
- Diagrama dos 3 componentes
- Caixa destaque: "Task = escopo | Action = método"
- Caixa destaque: "Goal: NÃO pule"
- Tabela quando usar / quando não usar
- Checklist "Antes de enviar seu TAG: ..."
Formato pronto para imprimir como PDF.
```

---

## Dica de uso

Carregue **apenas** os 3 arquivos listados no topo. Para comparação RACE vs TAG (prompts 6 e 7), adicione `docs/race.md` e `unidades/2-race/conteudo.md` temporariamente.