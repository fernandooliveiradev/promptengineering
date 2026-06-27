# Unidade 1 — Roteiro de Vídeo + Apresentação + Infográfico

> Duração-alvo do vídeo: 10-12 min
> Apresentação: ~12 slides
> Infográfico: 1 página A4, vertical

---

## PARTE A — Roteiro de vídeo (10-12 min)

### Bloco 1 — Abertura (1 min)

`[SLIDE 1 — abertura do curso + Unidade 1]`

**FALA:**
> Bem-vindo ao curso Prompt Engineering na Prática. Eu sou [nome] e nesta primeira unidade vamos responder: o que é prompt engineering e por que você deveria se importar?

`[SLIDE 2 — "fale sobre ia"]`

**FALA:**
> Você já digitou algo assim num ChatGPT? "Fale sobre IA". E o que veio? Provavelmente um textão genérico de 500 palavras que não serve para nada. O que faltou? **Engenharia de prompt.**

---

### Bloco 2 — Definição (2 min)

`[SLIDE 3 — fórmula M(p) → y ≈ y*]`

**FALA:**
> Em termos simples: dado um modelo M e um prompt p, o modelo gera uma saída y. Nosso objetivo é que y seja o mais próximo possível da resposta ideal y*. O prompt engineering é o processo de projetar p para maximizar essa chance.

`[PAUSA]`

**FALA:**
> Importante: o modelo é **probabilístico**, não determinístico. Não há prompt perfeito. Há prompts melhores e prompts piores. É uma mistura de arte e ciência.

`[SLIDE 4 — antes/depois]`

**FALA:**
> Veja a diferença. Antes: "fale sobre ia". Depois: "Explique IA para um leigo em 200 palavras, use uma analogia do cotidiano, termine com um exemplo prático que o leitor já tenha usado". A diferença na qualidade da resposta é dramática.

---

### Bloco 3 — Por que importa (1 min)

`[SLIDE 5 — 3 razões]`

**FALA:**
> Três razões para aprender isso agora. Primeiro: IA generativa já é ferramenta de trabalho. Segundo: a diferença entre usuário comum e alguém que sabe prompt engineering é de 10x em produtividade. Terceiro: é uma habilidade transferível — funciona com GPT, Claude, Gemini, qualquer LLM.

---

### Bloco 4 — Anatomia de um prompt (3 min)

`[SLIDE 6 — diagrama das 5 seções]`

**FALA:**
> Um prompt profissional tipicamente tem 5 seções, nessa ordem: Identidade, Instruções, Exemplos, Contexto, Entrada.

`[SLIDE 7 — Identidade + Instruções]`

**FALA:**
> Identidade: quem a IA deve ser. Quanto mais específico o domínio e senioridade, melhor. Instruções: o que fazer e o que NÃO fazer. Use verbos ativos.

`[SLIDE 8 — Exemplos + Contexto + Entrada]`

**FALA:**
> Exemplos: 3 a 5 entradas/saídas mostram o padrão. Contexto: dados de fundo — público, situação, restrições. Entrada: a tarefa específica deste turno.

---

### Bloco 5 — Regra de ouro + demo (2 min)

`[SLIDE 9 — regra de ouro]`

**FALA:**
> Regra de ouro: mostre seu prompt a um colega sem contexto. Se ele confundir, o modelo também confundirá. Seu colega é o teste mais barato que você tem.

`[MOSTRAR tela com prompt decomposto, destacando cada seção com cor diferente]`

**FALA:**
> Veja neste exemplo — destaquei cada seção com uma cor. Repare como a ordem ajuda o modelo a processar na sequência certa.

---

### Bloco 6 — Técnicas estabelecidas (2 min)

`[SLIDE 10 — tabela das 6 técnicas]`

**FALA:**
> Rápido nas 6 técnicas. Zero-shot: instrução direta, sem exemplos. Few-shot: 3-5 exemplos. Chain-of-thought: pensar passo a passo. Role prompting: dar persona. Structured output: pedir JSON. Prompt chaining: dividir tarefa em chamadas sequenciais.

`[MOSTRAR demo CoT — problema das máquinas/peças, com e sem CoT lado a lado]`

**FALA:**
> Veja este problema clássico. Sem CoT, o modelo erra. Com CoT — "pense passo a passo" — ele acerta. Compare as duas saídas.

---

### Bloco 7 — Fechamento (1 min)

`[SLIDE 11 — exercícios da unidade]`

**FALA:**
> Faça os 5 exercícios da unidade, listados no `conteudo.md`. Gabaritos no `exercicios.md`. Comece pelo 1.1 — reformular "fale sobre ia".

`[SLIDE 12 — próxima unidade]`

**FALA:**
> Na próxima unidade vamos conhecer o framework RACE — Role, Action, Context, Expectation. Até já.

---

## PARTE B — Outline da apresentação (12 slides)

| Slide | Título | Conteúdo principal | Elemento visual |
|---|---|---|---|
| 1 | Unidade 1 — Fundamentos | Logo do curso + título da unidade | Imagem de abertura |
| 2 | "Fale sobre ia" | Exemplo de prompt vago | Screenshot ChatGPT com resposta genérica |
| 3 | Definição formal | Fórmula M(p) → y ≈ y* | Diagrama da fórmula |
| 4 | Arte + ciência | Modelo probabilístico, não determinístico | Ícone balança (arte/ciência) |
| 5 | Antes vs depois | "fale sobre ia" vs versão específica | Comparação lado a lado |
| 6 | Por que importa | 3 razões em bullets | 3 ícones (trabalho, produtividade, transferível) |
| 7 | As 5 seções | Diagrama Identidade→Instruções→Exemplos→Contexto→Entrada | Diagrama de fluxo horizontal |
| 8 | Exemplo decomposto | Prompt do revisor de texto com seções coloridas | Screenshot com cores por seção |
| 9 | Regra de ouro | "Mostre a um colega sem contexto" | Ícone de colega + balão de pensamento |
| 10 | 6 técnicas estabelecidas | Tabela técnica × quando usar | Tabela compacta |
| 11 | Demo CoT | Problema das máquinas/peças com e sem CoT | Screenshot comparativo |
| 12 | Fechamento + exercícios | 5 exercícios + próxima unidade | Checklist + seta para Unidade 2 |

### Especificações visuais

- **Paleta:** usar a paleta do curso (definir 2 cores principais + 1 destaque)
- **Fontes:** 1 fonte título + 1 fonte corpo (máximo 2 fontes)
- **Densidade:** máx 6 linhas de texto por slide
- **Logo do curso:** canto inferior direito de cada slide
- **Numeração:** slide X/12 no canto inferior esquerdo

---

## PARTE C — Especificação do infográfico (1 página A4 vertical)

### Título
**"Anatomia de um Prompt Profissional — 5 Seções + 6 Técnicas"**

### Estrutura visual

```
┌─────────────────────────────────────┐
│  [LOGO CURSO]                       │
│                                     │
│  ANATOMIA DE UM PROMPT              │
│  PROFISSIONAL                       │
│  5 Seções + 6 Técnicas              │
│                                     │
│  ┌───────────────────────────────┐  │
│  │  AS 5 SEÇÕES (em ordem)       │  │
│  │                               │  │
│  │  1. IDENTIDADE  → quem é      │  │
│  │  2. INSTRUÇÕES  → o que fazer │  │
│  │  3. EXEMPLOS    → mostrar     │  │
│  │  4. CONTEXTO    → dados fundo │  │
│  │  5. ENTRADA     → tarefa now  │  │
│  └───────────────────────────────┘  │
│                                     │
│  ┌───────────────────────────────┐  │
│  │  AS 6 TÉCNICAS                │  │
│  │                               │  │
│  │  • Zero-shot   • Role         │  │
│  │  • Few-shot    • Structured   │  │
│  │  • CoT         • Chaining     │  │
│  └───────────────────────────────┘  │
│                                     │
│  ┌───────────────────────────────┐  │
│  │  REGRA DE OURO                │  │
│  │                               │  │
│  │  "Mostre seu prompt a um      │  │
│  │   colega sem contexto.        │  │
│  │   Se ele confundir, o modelo  │  │
│  │   também confundirá."         │  │
│  └───────────────────────────────┘  │
│                                     │
│  ANTES vs DEPOIS                    │
│  ❌ "fale sobre ia"                 │
│  ✅ "Explique IA para um leigo      │
│      em 200 palavras, use analogia, │
│      termine com exemplo prático."  │
│                                     │
│  [QR CODE para o curso]             │
└─────────────────────────────────────┘
```

### Especificações

- **Formato:** A4 vertical (210 × 297 mm)
- **Resolução:** 300 DPI (para impressão)
- **Cores:** paleta do curso
- **Fonte:** 1 fonte sans-serif legível (ex.: Inter, Roboto)
- **Hierarquia visual:** 3 blocos principais (5 seções, 6 técnicas, regra de ouro) + bloco antes/depois + QR code
- **Cores por seção (sugestão):**
  - 5 seções: gradiente de uma cor (do mais escuro ao mais claro, na ordem das seções)
  - 6 técnicas: cor de destaque secundária
  - Regra de ouro: caixa de destaque com cor de alerta (amarelo/dourado)
- **Ferramentas sugeridas:** Canva, Figma, Adobe Illustrator
- **Exportar em:** PDF (impressão) + PNG (redes sociais)

### Variações recomendadas

- **VersãoInstagram (1080×1080px):** só as 5 seções + regra de ouro (mais visual, menos texto)
- **Versão LinkedIn (1200×627px):** antes/depois + 6 técnicas em 2 colunas
- **Versão Stories (1080×1920px):** formato vertical esticado, mesmo conteúdo do A4