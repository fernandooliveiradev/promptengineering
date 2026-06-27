# Unidade 4 — Promontos para NotebookLM

> Carregue como fontes:
> - `docs/care.md`
> - `unidades/4-care/conteudo.md`
> - `exercicios.md` (exercícios 4.1 e 4.2)

---

## Prompt 1 — Guia de estudo da unidade

```
Crie um guia de estudo da Unidade 4 (Framework CARE — versão NN/G).
Organize em:
- Definição (1 linha)
- Por que adotamos a versão NN/G (não a do Prompt Edit)
- Os 4 componentes em 1 parágrafo cada (C, A, R, E)
- Quando usar (3 casos) e quando NÃO usar (3 casos)
- As 5 limitações documentadas pela própria NN/G
- 2 dicas práticas
```

---

## Prompt 2 — Quiz de 10 questões

```
Gere 10 questões de múltipla escolha (4 alternativas) sobre CARE:
- 2 sobre o significado de cada letra (Context, Ask, Rules, Examples)
- 2 sobre a diferença entre as duas versões de CARE (NN/G vs Prompt Edit)
- 2 sobre quando usar vs quando não usar
- 2 sobre as limitações documentadas pela NN/G
- 2 sobre pegadinhas (ex.: "Examples = few-shot?", "CARE é científico?")
Marque a resposta correta e justifique em 1 linha.
```

---

## Prompt 3 — Flashcards

```
Gere 12 flashcards "Frente: pergunta / Verso: resposta (máx 15 palavras)":
- 4 cards: o que significa C, A, R, E (versão NN/G)
- 2 cards: diferença NN/G vs Prompt Edit
- 2 cards: quando usar / quando não usar
- 2 cards: limitações documentadas pela NN/G
- 2 cards: pegadinhas (ex.: "Examples vs few-shot", "CARE dá trabalho?")
```

---

## Prompt 4 — Podcast (Audio Overview) da unidade

```
Crie um diálogo de podcast (2 apresentadores, ~7 min) sobre o framework CARE.
Estrutura:
1. Aviso: existem duas versões de CARE no mercado — explique
2. Por que adotamos a da NN/G (autoridade: Jakob Nielsen + Don Norman)
3. Os 4 componentes, com o exemplo das mensagens de erro de login (Kate Moran)
4. Por que Rules importa tanto (guardrails = qualidade)
5. Por que Examples é diferente de few-shot (segundo a NN/G)
6. As limitações honestas: "dá trabalho", às vezes custa mais tempo que fazer à mão
Tom didático. Termine com: "Na próxima unidade: ReAct, técnica acadêmica com paper peer-reviewed."
```

---

## Prompt 5 — Construção guiada de prompt CARE

```
Vou descrever uma tarefa de escrita profissional. Construa um prompt CARE
completo (versão NN/G) para ela. Para cada componente (C, A, R, E), explique
breve por que escolheu esse conteúdo. Inclua pelo menos 1 bom exemplo e 1
mau exemplo no componente Examples. Ao final, aponte 1 limitação potencial
deste prompt específico.
Tarefa: [descreva sua tarefa aqui]
```

---

## Prompt 6 — Crítica de prompt CARE

```
[Após colar um prompt CARE que você escreveu] Avalie este prompt verificando:
1. Quais dos 4 componentes (Context, Ask, Rules, Examples) estão presentes
   e bem construídos
2. Se Examples inclui bons E maus exemplos (diferencial do CARE)
3. Se Rules tem restrições observáveis (não vagas)
4. 3 sugestões concretas de melhoria
Formato: tabela para itens 1-3, lista para item 4.
```

---

## Prompt 7 — Comparação RACE vs CARE

```
Compare RACE (Unidade 2) e CARE (Unidade 4) em uma tabela única.
Colunas: componentes, complexidade, autoridade da fonte, quando usar,
exemplo de 1 linha. Explique em 2 linhas por que CARE é melhor que
RACE para tarefas onde tom e estilo importam (cartas de apresentação,
e-mails de vendas). Use o exemplo de Kate Moran para ilustrar.
```

---

## Prompt 8 — As 5 limitações do CARE (segundo NN/G)

```
Liste as 5 limitações/caveats que a própria Kate Moran (NN/G) documentou
para o CARE. Para cada uma:
1. Cite a limitação
2. Explique em 1 frase quando ela se manifesta
3. Dê 1 dica prática para mitigar
```

---

## Prompt 9 — FAQ da unidade

```
Gere um FAQ com 8 perguntas que um aluno faria sobre CARE:
- "Por que não usar a versão do Prompt Edit?"
- "Examples é o mesmo que few-shot?"
- "CARE serve para código?"
- "CARE é científico?"
- "Por que a NN/G diz que 'dá trabalho'?"
- "Rules pode ser longo?"
- "CARE vs RACE, qual usar?"
- "Precisa seguir a ordem C→A→R→E?"
Respostas em até 3 linhas.
```

---

## Prompt 10 — Síntese para revisão

```
Resuma a Unidade 4 em uma página A4 organizada em:
- Título: "Framework CARE (versão NN/G) — Context, Ask, Rules, Examples"
- Diagrama dos 4 componentes
- Caixa destaque: "Por que NN/G: autoridade em UX"
- Caixa destaque: "Cuidado: dá trabalho (segundo a própria NN/G)"
- Tabela quando usar / quando não usar
- Checklist "Antes de enviar seu CARE: ..."
Formato pronto para imprimir como PDF.
```

---

## Dica de uso

Carregue **apenas** os 3 arquivos listados no topo. Para comparação com RACE (prompt 7), adicione `docs/race.md` e `unidades/2-race/conteudo.md` temporariamente.