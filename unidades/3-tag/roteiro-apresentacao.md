# Unidade 3 — Roteiro de Vídeo + Apresentação + Infográfico

> Duração-alvo do vídeo: 8-10 min
> Apresentação: ~10 slides
> Infográfico: 1 página A4, vertical

---

## PARTE A — Roteiro de vídeo (8-10 min)

### Bloco 1 — Abertura (1 min)

`[SLIDE 1 — Unidade 3: Framework TAG]`

**FALA:**
> Na unidade anterior aprendemos o RACE. Hoje: o framework oposto. Quando RACE é over-engineering, você quer o TAG — o prompt mínimo viável.

`[SLIDE 2 — "menos é mais?"]`

**FALA:**
> Nem sempre mais é mais. Para tarefas simples, RACE pode ser exagero. TAG é três componentes focados: Task, Action, Goal.

---

### Bloco 2 — Definição (2 min)

`[SLIDE 3 — T·A·G]`

**FALA:**
> TAG: Task — o que fazer. Action — como fazer. Goal — o que é o sucesso. Três perguntas simples que respondem tudo.

`[SLIDE 4 — Características]`

**FALA:**
> TAG é o prompt mínimo viável. Custo de tokens baixo. Indicado para pedidos rápidos e bem definidos. Nível iniciante. A regra de ouro: nunca pule o Goal.

---

### Bloco 3 — Diferença crítica Task vs Action (2 min)

`[SLIDE 5 — Task vs Action]`

**FALA:**
> A pegadinha que mais confunde iniciantes: Task não é Action. Task é o **escopo** — a categoria do que precisa ser feito. Exemplo: "escreva um subject line". Action é o **método** — a instrução operacional específica. Exemplo: "gere cinco opções que criem urgência, máximo 50 caracteres".

`[PAUSA]`

**FALA:**
> Task é alto nível, focado em substantivo. Action é operacional, focado em verbo. Task define escopo; Action define método.

---

### Bloco 4 — Demo (3 min)

`[MOSTRAR prompt TAG completo para subject lines de reengajamento]`

**FALA:**
> Veja este exemplo. Task: escreva um subject line para campanha de reengajamento. Action: gere cinco opções que criem curiosidade e urgência sem ser clickbait. Goal: aumentar open rate entre assinantes inativos há 90 dias, cada subject line máximo 50 caracteres, funciona em mobile.

`[MOSTRAR a saída gerada pelo LLM]`

**FALA:**
> Veja a saída. Cinco subject lines curtos, com senso de urgência. Sem Goal, a IA poderia gerar subject lines genéricos sem pensar no público-alvo.

---

### Bloco 5 — Comparação RACE vs TAG (1 min)

`[SLIDE 6 — comparativo RACE vs TAG]`

**FALA:**
> Compare com o RACE da unidade anterior. TAG é ~30% menor. Perdeu o Role explícito e o Context dedicado. Para tarefas simples onde o contexto é evidente, TAG funciona melhor. Para tarefas profissionais com contexto rico, RACE vence.

---

### Bloco 6 — Quando usar (1 min)

`[SLIDE 7 — quando usar TAG]`

**FALA:**
> TAG é bom para: draft rápido, tradução, copy de marketing, geração de listas, reformatação. Não é bom para: fluxos multi-etapas complexos, tarefas que exigem persona detalhada, estratégia ou planejamento.

`[SLIDE 8 — prós e contras]`

**FALA:**
> Prós: mais rápido de escrever, fácil de lembrar, escala bem para tarefas repetitivas. Contras: sem Role (falta tom de especialista), sem Context dedicado.

---

### Bloco 7 — Exercício + fechamento (1 min)

`[SLIDE 9 — exercício 3.1]`

**FALA:**
> Faça o exercício 3.1: converta o prompt RACE da unidade anterior em TAG e compare as saídas. Qual foi melhor para este caso? Gabarito no `exercicios.md`.

`[SLIDE 10 — ponte para CARE]`

**FALA:**
> Para tarefas que precisam de mais contexto — comunicações profissionais, e-mails, propostas — temos o CARE. Próxima unidade. Até já.

---

## PARTE B — Outline da apresentação (10 slides)

| Slide | Título | Conteúdo principal | Elemento visual |
|---|---|---|---|
| 1 | Unidade 3 — Framework TAG | Logo do curso + título | Imagem de abertura |
| 2 | Menos é mais? | Quando RACE é over-engineering | Ícone balança |
| 3 | T·A·G | Os 3 componentes | Diagrama horizontal T→A→G |
| 4 | Características | Prompt mínimo viável, regra de ouro: não pule Goal | Caixa destaque "não pule Goal" |
| 5 | Task vs Action | A pegadinha mais comum, com exemplo | Comparação lado a lado |
| 6 | Demo subject lines | Prompt TAG do reengajamento | Screenshot com 3 componentes coloridos |
| 7 | RACE vs TAG | Comparativo visual | Tabela comparativa |
| 8 | Quando usar | 5 casos de uso | Ícones por caso |
| 9 | Prós e contras | 4 prós, 2 contras | Tabela |
| 10 | Exercício + ponte | Exercício 3.1 + próxima unidade CARE | Checklist + seta |

---

## PARTE C — Especificação do infográfico (1 página A4 vertical)

### Título
**"Framework TAG — Task, Action, Goal — O Prompt Mínimo Viável"**

### Estrutura visual

```
┌─────────────────────────────────────┐
│  [LOGO CURSO]                       │
│                                     │
│  FRAMEWORK TAG                      │
│  Task · Action · Goal               │
│  O Prompt Mínimo Viável             │
│                                     │
│  ┌───────────────────────────────┐  │
│  │  T — TASK                     │  │
│  │  O QUE fazer (alto nível)     │  │
│  │  "escreva um subject line"    │  │
│  └───────────────────────────────┘  │
│                                     │
│  ┌───────────────────────────────┐  │
│  │  A — ACTION                   │  │
│  │  COMO fazer (verbo específico)│  │
│  │  "gere 5 opções que criem     │  │
│  │   urgência, máx 50 caracteres"│  │
│  └───────────────────────────────┘  │
│                                     │
│  ┌───────────────────────────────┐  │
│  │  G — GOAL                     │  │  ← destaque amarelo
│  │  O QUE É O SUCESSO            │  │
│  │  "aumentar open rate em       │  │
│  │   inativos há 90 dias"        │  │
│  │                               │  │
│  │  ⚠ NÃO PULE O GOAL            │  │
│  └───────────────────────────────┘  │
│                                     │
│  ┌───────────────────────────────┐  │
│  │  TASK vs ACTION               │  │
│  │  Task = ESCOPO (alto nível)   │  │
│  │  Action = MÉTODO (operacional)│  │
│  └───────────────────────────────┘  │
│                                     │
│  QUANDO USAR                        │
│  ✓ Draft rápido                     │
│  ✓ Tradução                         │
│  ✓ Copy de marketing                │
│  ✓ Geração de listas                │
│                                     │
│  QUANDO NÃO USAR                    │
│  ✗ Multi-etapas → use RISE          │
│  ✗ Precisa persona → use RACE       │
│  ✗ Contexto rico → use CARE         │
│                                     │
│  TAG vs RACE                        │
│  TAG = 3 componentes, mais rápido   │
│  RACE = 4 componentes, mais rico    │
│                                     │
│  [QR CODE para o curso]             │
└─────────────────────────────────────┘
```

### Especificações

- **Formato:** A4 vertical (210 × 297 mm), 300 DPI
- **Cores:** paleta do curso + 1 caixa de destaque em amarelo/dourado para Goal
- **Cores por componente (sugestão):**
  - T: azul
  - A: verde
  - G: laranja + destaque amarelo

### Variações recomendadas

- **Versão Instagram (1080×1080px):** só as 3 caixas T/A/G + caixa "Task vs Action"
- **Versão LinkedIn (1200×627px):** diagrama T→A→G horizontal + tabela TAG vs RACE
- **Versão Stories (1080×1920px):** formato vertical, mesma estrutura do A4