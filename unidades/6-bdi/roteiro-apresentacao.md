# Unidade 6 — Roteiro de Vídeo + Apresentação + Infográfico

> Duração-alvo do vídeo: 10-12 min
> Apresentação: ~11 slides
> Infográfico: 1 página A4, vertical

---

## PARTE A — Roteiro de vídeo (10-12 min)

### Bloco 1 — Abertura (1 min)

`[SLIDE 1 — Unidade 6: BDI]`

**FALA:**
> Na unidade anterior vimos ReAct, para tarefas que precisam de informação externa. Hoje: BDI, para tarefas que precisam de um agente com estado interno.

`[SLIDE 2 — "e quando precisa de um agente com estado interno?"]`

**FALA:**
> ReAct lida com informação externa. Mas e quando precisamos simular um agente com objetivos, crenças e planos? Aí entra o BDI.

---

### Bloco 2 — Definição + aviso importante (2 min)

`[SLIDE 3 — BDI: Belief-Desire-Intention]`

**FALA:**
> BDI significa Belief, Desire, Intention. É um modelo de software para agentes racionais, proposto por Rao e Georgeff em 1995, baseado na filosofia de Michael Bratman de 1987.

`[SLIDE 4 — aviso: BDI não é framework de prompt]`

**FALA:**
> Importante: BDI **não** é um framework de prompt. É um modelo de arquitetura de agentes de software. Vamos usá-lo como **analogia** para prompts, mas o uso original é outro. Isso é honestidade acadêmica — não vou vender BDI como técnica de prompt quando ele não é.

---

### Bloco 3 — Os três componentes (3 min)

`[SLIDE 5 — Beliefs]`

**FALA:**
> Beliefs: o que o agente sabe sobre o mundo. Em prompts: fatos, regras do domínio, dados do caso. Exemplo: "inflação 4,5%, juros cartão 12%/mês".

`[SLIDE 6 — Desires]`

**FALA:**
> Desires: o que o agente gostaria de alcançar. Em prompts: os objetivos da tarefa. Exemplo: "recomendar melhor alocação entre quitar dívida e investir".

`[SLIDE 7 — Intentions]`

**FALA:**
> Intentions: o que o agente escolheu fazer — os planos concretos. Em prompts: os passos numerados que a IA deve seguir. Exemplo: "1. Calcular custo da dívida; 2. Calcular ganho do investimento; 3. Comparar".

---

### Bloco 4 — Ciclo do interpretador (2 min)

`[SLIDE 8 — ciclo BDI]`

**FALA:**
> O ciclo do interpretador BDI é: perceber o ambiente, revisar crenças, gerar desejos, selecionar intenções, executar plano, capturar novos eventos, abandonar atitudes malsucedidas ou impossíveis. Repete.

`[PAUSA]`

**FALA:**
> Não precisa decorar o ciclo — o que importa é a ideia: agente com estado interno que delibera antes de agir.

---

### Bloco 5 — Demo (2 min)

`[MOSTRAR prompt BDI para planejador financeiro (dívida vs investimento)]`

**FALA:**
> Veja este exemplo. Beliefs traz os fatos econômicos (juros, inflação) + perfil do usuário. Desires traz os objetivos. Intentions traz os 5 passos concretos. Repare como a estrutura obriga o modelo a raciocinar com estado interno.

`[MOSTRAR a saída gerada pelo LLM]`

**FALA:**
> Veja a saída. O modelo calcula juros compostos, compara com investimento, recomenda com justificativa econômica. Isso é difícil de conseguir com um prompt RACE simples — BDI força o raciocínio estruturado.

---

### Bloco 6 — Quando usar + limitações (1 min)

`[SLIDE 9 — quando usar BDI]`

**FALA:**
> Use a analogia BDI quando a tarefa exigir um agente com objetivos, regras internas e tomada de decisão estruturada — assistente jurídico, planejador financeiro, tutor de idiomas. Limitação: é complexo. Para tarefas cotidianas, RACE ou CARE bastam.

---

### Bloco 7 — Exercício + fechamento (1 min)

`[SLIDE 10 — exercício 6.1]`

**FALA:**
> Faça o exercício 6.1: construa um prompt BDI para um planejador financeiro. Gabarito no `exercicios.md`.

`[SLIDE 11 — ponte para rúbricas]`

**FALA:**
> Vimos 5 frameworks/técnicas: RACE, TAG, CARE, ReAct, BDI. Mas como avaliar se um prompt é bom? Aí entram as rúbricas, próxima unidade. Até já.

---

## PARTE B — Outline da apresentação (11 slides)

| Slide | Título | Conteúdo principal | Elemento visual |
|---|---|---|---|
| 1 | Unidade 6 — BDI | Logo do curso + título | Imagem de abertura |
| 2 | Quando precisa de agente com estado interno? | Limite do ReAct | Ícone agente |
| 3 | BDI: Belief-Desire-Intention | Definição + origem | Diagrama 3 componentes |
| 4 | Aviso: BDI não é framework de prompt | É modelo de agentes | Caixa amarela de aviso |
| 5 | Beliefs | Fatos, regras, dados do caso | Caixa com exemplo |
| 6 | Desires | Objetivos da tarefa | Caixa com exemplo |
| 7 | Intentions | Passos concretos numerados | Caixa com exemplo |
| 8 | Ciclo do interpretador | 7 passos em diagrama | Diagrama circular |
| 9 | Demo planejador financeiro | Prompt BDI completo + saída | Screenshot com seções coloridas |
| 10 | Quando usar + limitações | 4 casos de uso + 3 limitações | Tabela + ícones |
| 11 | Exercício + ponte | Exercício 6.1 + rúbricas a seguir | Checklist + seta |

---

## PARTE C — Especificação do infográfico (1 página A4 vertical)

### Título
**"BDI — Belief, Desire, Intention (Bratman 1987; Rao & Georgeff 1995)"**

### Estrutura visual

```
┌─────────────────────────────────────┐
│  [LOGO CURSO]                       │
│                                     │
│  BDI                                │
│  Belief · Desire · Intention        │
│  Modelo de Agentes Racionais        │
│                                     │
│  ┌───────────────────────────────┐  │
│  │  ⚠ BDI NÃO É FRAMEWORK DE    │  │  ← destaque amarelo
│  │  PROMPT — é modelo de agentes │  │
│  │  Usamos como ANALOGIA         │  │
│  └───────────────────────────────┘  │
│                                     │
│  ORIGEM ACADÊMICA                   │
│  • Bratman 1987 (filosofia)         │
│  • Rao & Georgeff 1995 (IA)         │
│  • Extensões: BDICTL, LORA          │
│  • Implementações: PRS, Jason,      │
│    JaCaMo (ativas em 2026)          │
│                                     │
│  ┌───────────────────────────────┐  │
│  │  B — BELIEFS                  │  │
│  │  O que o agente SABE          │  │
│  │  Em prompts: fatos, regras,   │  │
│  │  dados do caso                │  │
│  └───────────────────────────────┘  │
│                                     │
│  ┌───────────────────────────────┐  │
│  │  D — DESIRES                  │  │
│  │  O que o agente QUER          │  │
│  │  Em prompts: objetivos        │  │
│  └───────────────────────────────┘  │
│                                     │
│  ┌───────────────────────────────┐  │
│  │  I — INTENTIONS               │  │
│  │  O que o agente VAI FAZER     │  │
│  │  Em prompts: passos numerados │  │
│  └───────────────────────────────┘  │
│                                     │
│  CICLO DO INTERPRETADOR             │
│  Perceber → Revisar crenças →       │
│  Gerar desejos → Selecionar         │
│  intenções → Executar → Capturar    │
│  eventos → Abandonar inviáveis      │
│                                     │
│  QUANDO USAR (analogia)             │
│  ✓ Assistente jurídico              │
│  ✓ Planejador financeiro            │
│  ✓ Tutor de idiomas                 │
│  ✓ Médico diagnóstico               │
│                                     │
│  LIMITAÇÕES                         │
│  ✗ Complexo — RACE/CARE bastam      │
│    para tarefas cotidianas          │
│  ✗ Analogia, não uso original      │
│                                     │
│  BDI vs ReAct                       │
│  ReAct: acesso externo              │
│  BDI: estado interno estruturado    │
│                                     │
│  [QR CODE para o curso]             │
└─────────────────────────────────────┘
```

### Especificações

- **Formato:** A4 vertical (210 × 297 mm), 300 DPI
- **Cores:** paleta do curso + 1 caixa de destaque amarelo ("BDI não é framework de prompt")
- **Cores por componente (sugestão):**
  - B: azul
  - D: verde
  - I: laranja

### Variações recomendadas

- **Versão Instagram (1080×1080px):** 3 caixas B/D/I + caixa "aviso: não é prompt framework"
- **Versão LinkedIn (1200×627px):** diagrama B→D→I + ciclo do interpretador
- **Versão Stories (1080×1920px):** formato vertical, mesma estrutura do A4