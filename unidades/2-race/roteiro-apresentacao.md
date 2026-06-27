# Unidade 2 — Roteiro de Vídeo + Apresentação + Infográfico

> Duração-alvo do vídeo: 8-10 min
> Apresentação: ~10 slides
> Infográfico: 1 página A4, vertical

---

## PARTE A — Roteiro de vídeo (8-10 min)

### Bloco 1 — Abertura (1 min)

`[SLIDE 1 — Unidade 2: Framework RACE]`

**FALA:**
> Na unidade anterior vimos técnicas isoladas. Hoje vamos organizá-las num framework memorável: RACE. Role, Action, Context, Expectation.

`[SLIDE 2 — "framework" como organização]`

**FALA:**
> Framework não é uma técnica nova — é uma estrutura que organiza as técnicas que você já conhece em algo fácil de lembrar e aplicar. RACE é o mais versátil dos frameworks práticos.

---

### Bloco 2 — Definição (3 min)

`[SLIDE 3 — R·A·C·E]`

**FALA:**
> RACE: quatro componentes memoráveis. R de Role — quem a IA deve ser. A de Action — o que fazer. C de Context — o contexto de fundo. E de Expectation — o formato e qualidade esperados.

`[SLIDE 4 — R: Role]`

**FALA:**
> Role: a persona. Não diga "você é um designer". Diga "você é um UX designer sênior com 10 anos em mobile". Especificidade de domínio e senioridade importa.

`[SLIDE 5 — A: Action]`

**FALA:**
> Action: o que fazer, com verbo ativo. "Escreva", "resuma", "compare", "depure". Evite "me ajude com" — é vago demais.

`[SLIDE 6 — C: Context]`

**FALA:**
> Context: o componente mais pulado e o maior responsável por saídas genéricas. Inclua público, restrições, situação. Sem Context, a IA responde no genérico.

`[SLIDE 7 — E: Expectation]`

**FALA:**
> Expectation: o formato, extensão, tom. É o que mais controla a qualidade da saída. Inclua critérios mensuráveis: "máximo 150 palavras", "3 opções", "sem jargão".

---

### Bloco 3 — Demo (3 min)

`[MOSTRAR prompt RACE completo na tela, com cada componente destacado por cor]`

**FALA:**
> Veja este exemplo de prompt RACE para um e-mail de follow-up após entrevista. Repare: Role específico (coach de carreira sênior), Action com verbo ativo (escreva um e-mail), Context com 4 detalhes (entrevista há 2 dias, fintech, recrutadora Marina, 7 dias úteis), Expectation com formato + extensão + tom + critério mensurável (máximo 150 palavras, CTA sutil).

`[MOSTRAR a saída gerada pelo LLM]`

**FALA:**
> Veja a saída. Profissional, concisa, menciona o ponto específico da entrevista, tem CTA sutil. RACE funciona.

---

### Bloco 4 — Quando usar + limitações (1 min)

`[SLIDE 8 — quando usar RACE]`

**FALA:**
> RACE é bom para escrita profissional, e-mails, resumos, code review. É versátil. Não é bom para tarefas muito simples — aí usamos TAG, que veremos na próxima unidade.

`[SLIDE 9 — prós e contras]`

**FALA:**
> RACE é fácil de memorizar e funciona em qualquer domínio. Limitação: não tem slot dedicado para exemplos. Se você precisa de exemplo, adicione manualmente — ou use CARE, que veremos na Unidade 4.

---

### Bloco 5 — Exercício (1 min)

`[SLIDE 10 — exercício 2.1]`

**FALA:**
> Faça o exercício 2.1: construa um prompt RACE para um e-mail de follow-up. Gabarito no `exercicios.md`. Na próxima unidade, vamos conhecer o TAG — o prompt mínimo viável, pra quando RACE é over-engineering. Até já.

---

## PARTE B — Outline da apresentação (10 slides)

| Slide | Título | Conteúdo principal | Elemento visual |
|---|---|---|---|
| 1 | Unidade 2 — Framework RACE | Logo do curso + título | Imagem de abertura |
| 2 | Por que framework? | Framework organiza técnicas em estrutura memorável | Ícone estrutura |
| 3 | R·A·C·E | Os 4 componentes em diagrama | Diagrama horizontal R→A→C→E |
| 4 | R — Role | Persona específica, com exemplo bom e ruim | Comparação bom/ruim |
| 5 | A — Action | Verbo ativo, com exemplo bom e ruim | Comparação bom/ruim |
| 6 | C — Context | O componente mais pulado, com exemplo | Caixa de destaque "mais pulado" |
| 7 | E — Expectation | O que mais controla qualidade, com exemplo | Caixa de destaque "mais impacto" |
| 8 | Demo completa | Prompt RACE do e-mail de follow-up com seções coloridas | Screenshot com cores |
| 9 | Quando usar + limitações | 5 casos de uso + 2 limitações | Tabela + ícones |
| 10 | Exercício + ponte | Exercício 2.1 + próxima unidade TAG | Checklist + seta |

---

## PARTE C — Especificação do infográfico (1 página A4 vertical)

### Título
**"Framework RACE — Role, Action, Context, Expectation"**

### Estrutura visual

```
┌─────────────────────────────────────┐
│  [LOGO CURSO]                       │
│                                     │
│  FRAMEWORK RACE                     │
│  Role · Action · Context ·          │
│  Expectation                        │
│                                     │
│  ┌───────────────────────────────┐  │
│  │  R — ROLE                     │  │
│  │  Quem a IA deve ser           │  │
│  │  ❌ "você é um designer"      │  │
│  │  ✅ "você é um UX designer    │  │
│  │      sênior com 10 anos em    │  │
│  │      mobile"                  │  │
│  └───────────────────────────────┘  │
│                                     │
│  ┌───────────────────────────────┐  │
│  │  A — ACTION                   │  │
│  │  O que fazer (verbo ativo)    │  │
│  │  ❌ "me ajude com..."         │  │
│  │  ✅ "escreva um e-mail de     │  │
│  │      follow-up"               │  │
│  └───────────────────────────────┘  │
│                                     │
│  ┌───────────────────────────────┐  │
│  │  C — CONTEXT                  │  │
│  │  O componente MAIS PULADO     │  │  ← destaque amarelo
│  │  Público, restrições, situação│  │
│  └───────────────────────────────┘  │
│                                     │
│  ┌───────────────────────────────┐  │
│  │  E — EXPECTATION              │  │
│  │  O que MAIS CONTROLA QUALIDADE│  │  ← destaque amarelo
│  │  Formato, extensão, tom       │  │
│  └───────────────────────────────┘  │
│                                     │
│  QUANDO USAR                        │
│  ✓ E-mails profissionais            │
│  ✓ Resumos de pesquisa              │
│  ✓ Code review                      │
│  ✓ Explicações educacionais         │
│                                     │
│  QUANDO NÃO USAR                    │
│  ✗ Tarefas simples → use TAG        │
│  ✗ Precisa de exemplo → use CARE    │
│                                     │
│  [QR CODE para o curso]             │
└─────────────────────────────────────┘
```

### Especificações

- **Formato:** A4 vertical (210 × 297 mm)
- **Resolução:** 300 DPI
- **Cores:** paleta do curso + 2 caixas de destaque em amarelo/dourado para "mais pulado" e "mais controla qualidade"
- **Hierarquia visual:** 4 caixas (R, A, C, E) + 2 caixas menor (quando usar / não usar)
- **Cores por componente (sugestão):**
  - R: azul
  - A: verde
  - C: laranja + destaque amarelo
  - E: vermelho + destaque amarelo

### Variações recomendadas

- **Versão Instagram (1080×1080px):** só as 4 caixas R/A/C/E com exemplos bom/ruim
- **Versão LinkedIn (1200×627px):** diagrama R→A→C→E horizontal + tabela quando usar
- **Versão Stories (1080×1920px):** formato vertical, mesma estrutura do A4