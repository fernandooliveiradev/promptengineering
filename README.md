# Prompt Engine — Documentação de Apoio

> Coletânea de documentação profissional para cursos online sobre prompt engineering e frameworks relacionados.
> Todos os links foram verificados como ativos em junho de 2026.

---

## Índice

| Documento | Tipo | Fonte principal verificada |
|---|---|---|
| [prompt-engineering.md](docs/prompt-engineering.md) | Conceito geral | OpenAI, Anthropic, DAIR.AI, Learn Prompting |
| [race.md](docs/race.md) | Framework de prompt (heurística) | Prompt Edit (promptedit.app) |
| [tag.md](docs/tag.md) | Framework de prompt (heurística) | Prompt Edit + PromptVibe (convergentes) |
| [care.md](docs/care.md) | Framework de prompt (heurística) | **Nielsen Norman Group** (Kate Moran, mai/2024) — autoridade principal |
| [react.md](docs/react.md) | Framework de prompt (acadêmico) | Yao et al. 2022 (arXiv:2210.03629) |
| [bdi.md](docs/bdi.md) | Modelo de agentes (acadêmico) | Wikipedia + Emergent Mind |
| [rubrica.md](docs/rubrica.md) | Avaliação — conceito e prática | Carnegie Mellon (Eberly Center) + Wikipedia |

---

## Classificação por nível de evidência

### Frameworks de prompt (heurísticas práticas mnemônicas)
- **RACE** — Role, Action, Context, Expectation
- **TAG** — Task, Action, Goal
- **CARE** — Context, Ask, Rules, Examples (versão NN/G — autoridade principal)

> Estes frameworks são **técnicas práticas derivadas das melhores práticas de prompt engineering**, sem paper acadêmico original que os formalize. São compatíveis com as técnicas estabelecidas (role prompting, few-shot, structured output) documentadas pelas fontes oficiais (OpenAI, Anthropic, DAIR.AI, Learn Prompting).
>
> **Observação sobre CARE:** existe uma variante concorrente (Context, Action, Result, Example) no Prompt Edit. Adotamos a versão da **Nielsen Norman Group** por ser a fonte de maior autoridade (empresa de pesquisa de UX reconhecida internacionalmente, fundada por Jakob Nielsen e Don Norman; artigo assinado por Kate Moran em maio/2024). Ver detalhes em `docs/care.md`, seção 10.

### Frameworks/técnicas com fundamentação acadêmica
- **ReAct** — paper peer-reviewed (Yao et al., 2022), reconhecido por todas as fontes autoritativas
- **BDI** — modelo teórico formal (Bratman 1987; Rao & Georgeff 1995), com lógica modal/temporal (BDICTL, LORA) e implementações de software ativas em 2026

---

## Observação de transparência metodológica

Os frameworks RACE, TAG e CARE **não aparecem em fontes acadêmicas peer-reviewed** nem na documentação oficial dos fabricantes de LLMs (OpenAI, Anthropic). Foram encontrados em **sites especializados** (Prompt Edit — promptedit.app), mantido por Sebastian Messingfeld (Cologne, Alemanha), que cataloga 50+ frameworks de prompt.

Para um curso acadêmico, recomenda-se:
- **Apresentar RACE/TAG/CARE como heurísticas práticas**, não como técnicas cientificamente validadas.
- **Complementar com ReAct e BDI** para fornecer embasamento acadêmico.
- **Citar sempre as fontes verificadas** indicadas em cada documento.

---

## Como usar este material

1. Comece por `prompt-engineering.md` para fundamentos gerais.
2. Para cursos práticos introdutórios: RACE → TAG → CARE (do mais completo ao mais minimalista).
3. Para cursos avançados/acadêmicos: ReAct (paper) e BDI (arquitetura de agentes).
4. Cada arquivo `.md` é autossuficiente e pode ser usado como material de leitura isolado.# promptengineering
