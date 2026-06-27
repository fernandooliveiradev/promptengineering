# Unidade 5 — Roteiro de Vídeo + Apresentação + Infográfico

> Duração-alvo do vídeo: 10-12 min
> Apresentação: ~11 slides
> Infográfico: 1 página A4, vertical

---

## PARTE A — Roteiro de vídeo (10-12 min)

### Bloco 1 — Abertura (1 min)

`[SLIDE 1 — Unidade 5: ReAct]`

**FALA:**
> Até agora vimos frameworks práticos: RACE, TAG, CARE. Heurísticas sem paper acadêmico. Hoje a primeira técnica com embasamento científico: ReAct.

`[SLIDE 2 — "e quando precisa buscar informação?"]`

**FALA:**
> Os frameworks práticos operam com conhecimento interno do modelo. E quando a tarefa precisa de informação externa? Conheça ReAct.

---

### Bloco 2 — Definição + origem (2 min)

`[SLIDE 3 — ReAct = Reasoning + Acting]`

**FALA:**
> ReAct é um framework proposto por Yao e colegas em 2022, num paper acadêmico peer-reviewed disponível em arXiv. Combina raciocínio e ação de forma intercalada.

`[SLIDE 4 — diferencial acadêmico]`

**FALA:**
> Diferencial: tem paper, tem resultados empíricos em benchmarks públicos (HotpotQA, Fever, ALFWorld, WebShop), tem implementação em bibliotecas de mercado como LangChain. É a primeira técnica do curso com embasamento científico.

---

### Bloco 3 — Motivação (2 min)

`[SLIDE 5 — CoT vs Acting vs ReAct]`

**FALA:**
> Por que ReAct existe? Chain-of-thought raciocinha mas não acessa o mundo externo — alucina fatos. Acting puro age mas não raciocina — falha em decompor metas. ReAct pega o melhor dos dois: raciocínio para planejar, ação para obter evidências.

---

### Bloco 4 — Como funciona (3 min)

`[SLIDE 6 — trajetória Thought/Action/Observation]`

**FALA:**
> A trajetória é: Thought — raciocínio. Action — chamada a ferramenta. Observation — resultado da ferramenta. Repetir até chegar à resposta.

`[MOSTRAR exemplo da trajetória do paper: pergunta sobre Colorado orogeny]`

**FALA:**
> Veja o exemplo clássico do paper. O modelo raciocina: "preciso buscar Colorado orogeny". Age: faz Search. Observa: lê resultado. Raciocina de novo. Cada Thought guia o próximo Action. A ideia central: raciocínio orienta o que buscar; busca fornece evidências que sustentam o raciocínio.

---

### Bloco 5 — Resultados empíricos (1 min)

`[SLIDE 7 — HotpotQA, Fever, ALFWorld, WebShop]`

**FALA:**
> Resultados: ReAct supera acting puro em todos os benchmarks. Às vezes supera CoT, às vezes fica atrás — os melhores resultados vêm de combinar ReAct + CoT + self-consistency.

---

### Bloco 6 — Implementação (1 min)

`[SLIDE 8 — LangChain]`

**FALA:**
> Na prática, ReAct é o padrão de agente em bibliotecas como LangChain. Você não escreve a trajetória à mão — o framework orquestra. Cinco linhas de Python e você tem um agente ReAct funcional.

---

### Bloco 7 — Limitações (1 min)

`[SLIDE 9 — limitações]`

**FALA:**
> Limitações honestas: depende da qualidade das ferramentas externas — buscas pouco informativas descarrilam o raciocínio. Restrição estrutural — o formato reduz flexibilidade. Recuperação limitada após erro. Ainda abaixo do desempenho humano em tarefas complexas.

---

### Bloco 8 — Exercício + fechamento (1 min)

`[SLIDE 10 — exercício 5.1]`

**FALA:**
> Faça o exercício 5.1: escreva a trajetória ReAct para "Qual o PIB per capita do país onde nasceu o criador do Python?". Gabarito no `exercicios.md`.

`[SLIDE 11 — ponte para BDI]`

**FALA:**
> ReAct lida com informação externa. Mas e quando precisamos simular um agente com estado interno, crenças e objetivos? Aí entra o BDI, próxima unidade. Até já.

---

## PARTE B — Outline da apresentação (11 slides)

| Slide | Título | Conteúdo principal | Elemento visual |
|---|---|---|---|
| 1 | Unidade 5 — ReAct | Logo do curso + título | Imagem de abertura |
| 2 | Quando precisa buscar informação? | Limite dos frameworks práticos | Ícone busca |
| 3 | ReAct = Reasoning + Acting | Definição + origem (Yao 2022) | Diagrama Reasoning + Acting |
| 4 | Diferencial acadêmico | Paper, benchmarks, LangChain | Caixa destaque "peer-reviewed" |
| 5 | CoT vs Acting vs ReAct | Tabela comparativa dos limites | Tabela 3 colunas |
| 6 | Trajetória Thought/Action/Observation | Diagrama do fluxo | Diagrama circular |
| 7 | Exemplo Colorado orogeny | Trajetória completa do paper | Screenshot com cores por etapa |
| 8 | Resultados empíricos | 4 benchmarks + conclusão | Tabela de resultados |
| 9 | Implementação LangChain | Código Python (5 linhas) | Screenshot código |
| 10 | Limitações | 4 limitações documentadas | Caixa amarela |
| 11 | Exercício + ponte | Exercício 5.1 + BDI a seguir | Checklist + seta |

---

## PARTE C — Especificação do infográfico (1 página A4 vertical)

### Título
**"ReAct — Reasoning + Acting (Yao et al., 2022)"**

### Estrutura visual

```
┌─────────────────────────────────────┐
│  [LOGO CURSO]                       │
│                                     │
│  ReAct                              │
│  Reasoning + Acting                 │
│  Yao et al., 2022 — arXiv:2210.03629│
│                                     │
│  ┌───────────────────────────────┐  │
│  │  ⚠ PRIMEIRA TÉCNICA DO CURSO  │  │  ← destaque amarelo
│  │  COM PAPER PEER-REVIEWED      │  │
│  └───────────────────────────────┘  │
│                                     │
│  POR QUE ReAct?                     │
│  ┌──────────┬──────────┬─────────┐  │
│  │ CoT puro │ Acting   │ ReAct   │  │
│  │ alucina  │ puro não │ combina │  │
│  │ fatos    │ raciocina│ os dois │  │
│  └──────────┴──────────┴─────────┘  │
│                                     │
│  TRAJETÓRIA                         │
│  ┌───────────────────────────────┐  │
│  │  Thought N → raciocínio       │  │
│  │  Action N  → ferramenta       │  │
│  │  Observation N → resultado    │  │
│  │  ...                          │  │
│  │  Finish[resposta final]       │  │
│  └───────────────────────────────┘  │
│                                     │
│  EXEMPLO (1 passo)                  │
│  Thought: "Preciso buscar X"        │
│  Action: Search[X]                  │
│  Observation: "X é..."              │
│                                     │
│  RESULTADOS EMPÍRICOS               │
│  ✓ Superou Acting em todos          │
│  ✓ Superou CoT em Fever             │
│  ~ Empatou/atrás em HotpotQA        │
│  ★ Melhor: ReAct + CoT + Self-Cons. │
│                                     │
│  QUANDO USAR                        │
│  ✓ Tarefa precisa de info externa   │
│  ✓ Tomada de decisão multi-etapas   │
│  ✓ Precisa de auditabilidade        │
│                                     │
│  LIMITAÇÕES                         │
│  ✗ Depende da qualidade das buscas  │
│  ✗ Recuperação limitada após erro   │
│  ✗ Abaixo do humano em tarefas      │
│    complexas                        │
│                                     │
│  IMPLEMENTAÇÃO                      │
│  LangChain: 5 linhas de Python      │
│  agent = initialize_agent(tools,    │
│    llm, agent="zero-shot-react")    │
│                                     │
│  [QR CODE para o curso]             │
└─────────────────────────────────────┘
```

### Especificações

- **Formato:** A4 vertical (210 × 297 mm), 300 DPI
- **Cores:** paleta do curso + 1 caixa de destaque amarelo ("primeira técnica peer-reviewed")
- **Hierarquia visual:** caixa destaque + 3 blocos comparativos + trajetória + resultados + quando usar + limitações + implementação

### Variações recomendadas

- **Versão Instagram (1080×1080px):** trajetória Thought/Action/Observation + comparação CoT/Acting/ReAct
- **Versão LinkedIn (1200×627px):** diagrama ReAct + tabela resultados empíricos
- **Versão Stories (1080×1920px):** formato vertical, mesma estrutura do A4