# Unidade 2 — Promontos para NotebookLM

> Carregue como fontes:
> - `docs/race.md`
> - `unidades/2-race/conteudo.md`
> - `exercicios.md` (exercícios 2.1 e 2.2)

---

## Prompt 1 — Guia de estudo da unidade

```
Crie um guia de estudo da Unidade 2 (Framework RACE). Organize em:
- Definição (1 linha)
- Os 4 componentes explicados em 1 parágrafo cada (R, A, C, E)
- Quando usar (3 casos)
- 3 dicas práticas que mais impactam a qualidade do prompt RACE
- 2 erros comuns ao usar RACE
```

---

## Prompt 2 — Quiz de 8 questões

```
Gere 8 questões de múltipla escolha (4 alternativas) sobre o framework RACE:
- 2 sobre o significado de cada letra
- 2 sobre quando usar vs quando não usar
- 2 sobre os componentes mais críticos (Context e Expectation)
- 2 sobre pegadinhas (ex.: "Role genérico vs específico", "Expectation negativa vs positiva")
Marque a resposta correta e justifique em 1 linha.
```

---

## Prompt 3 — Flashcards

```
Gere 10 flashcards "Frente: pergunta / Verso: resposta (máx 15 palavras)" sobre RACE:
- 4 cards: o que significa R, A, C, E
- 2 cards: quando usar / quando NÃO usar
- 2 cards: prós e contras
- 2 cards: pegadinhas (ex.: "Task vs Action", "Role genérico vs específico")
```

---

## Prompt 4 — Podcast (Audio Overview) da unidade

```
Crie um diálogo de podcast (2 apresentadores, ~6 min) sobre o framework RACE.
Estrutura:
1. Por que usar um framework (vs prompt solto)
2. Os 4 componentes, com o exemplo do UX writer reescrevendo "Error 403"
3. Por que Context é o componente mais pulado e mais importante
4. Por que Expectation é o que mais controla a qualidade
5. Quando RACE é over-engineering (ponte para TAG)
Tom didático. Termine com: "Na próxima unidade: TAG, o prompt mínimo viável."
```

---

## Prompt 5 — Construção guiada de prompt RACE

```
Vou descrever uma tarefa. Construa um prompt RACE completo para ela.
Para cada componente (R, A, C, E), explique brevemente por que escolheu
esse conteúdo. Ao final, dê 1 alternativa de melhoria para o componente
mais fraco.
Tarefa: [descreva sua tarefa aqui]
```

---

## Prompt 6 — Crítica de prompt RACE

```
[Após colar um prompt RACE que você escreveu] Avalie este prompt usando
a rúbrica RACE (seção 8.3 do rubrica.md). Para cada componente (R, A, C, E),
dê nota de 1 a 4 e justifique citando trecho do prompt. Sugira 3 melhorias
concretas, uma por componente fraco.
```

---

## Prompt 7 — Comparação RACE vs RTF

```
Compare RACE e RTF (Role, Task, Format) em uma tabela única.
Colunas: componentes, complexidade, quando usar, exemplo de 1 linha.
Explique em 2 linhas por que RACE costuma produzir melhores resultados
que RTF, mesmo sendo parecidos. Use como base o exemplo do e-mail de
follow-up para ilustrar a diferença.
```

---

## Prompt 8 — Quando NÃO usar RACE

```
Liste 5 situações em que RACE é over-engineering e outro framework seria
melhor. Para cada situação, indique o framework alternativo e por quê.
Baseie-se na comparação com TAG (Unidade 3) e CARE (Unidade 4).
```

---

## Prompt 9 — FAQ da unidade

```
Gere um FAQ com 6 perguntas que um aluno faria sobre RACE:
- "Role é sempre necessário?"
- "Context pode ser longo?"
- "Expectation é o mesmo que formato?"
- "RACE serve para código?"
- "RACE é científico?"
- "RACE vs TAG, qual usar?"
Respostas em até 3 linhas.
```

---

## Prompt 10 — Síntese para revisão

```
Resuma a Unidade 2 em uma página A4 organizada em:
- Título: "Framework RACE — Role, Action, Context, Expectation"
- Diagrama dos 4 componentes em sequência
- Tabela "quando usar" (3 casos)
- Caixa de destaque: "Context é o componente mais pulado"
- Caixa de destaque: "Expectation é o que mais controla qualidade"
- Checklist "Antes de enviar seu RACE: ..."
Formato pronto para imprimir como PDF.
```

---

## Dica de uso

Carregue **apenas** os 3 arquivos listados no topo. Para a comparação RACE vs TAG (prompt 8), você pode adicionar `docs/tag.md` temporariamente.