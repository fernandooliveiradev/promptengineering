# Plano de Curso — Prompt Engineering na Prática

> Curso online de prompt engineering baseado na documentação verificada em `docs/`.
> Nível: iniciante-intermediário · Carga horária estimada: 20h (12h teoria + 8h prática)
> Modalidade: videoaulas + exercícios + projeto final

---

## 1. Público-alvo

- Profissionais que usam IA generativa no trabalho (redatores, desenvolvedores, analistas, designers, gestores)
- Estudantes e pesquisadores que querem usar LLMs com rigor
- Instrutores que precisam criar material de prompt engineering para suas turmas

**Pré-requisitos:** familiaridade básica com ChatGPT, Claude ou Gemini. Nenhuma programação é exigida.

---

## 2. Competências a serem desenvolvidas

Ao concluir o curso, o aluno será capaz de:

1. Explicar o que é prompt engineering e por que é mistura de arte e ciência.
2. Aplicar frameworks de prompt (RACE, TAG, CARE) a tarefas reais.
3. Escolher o framework adequado ao tipo de tarefa.
4. Construir prompts usando a técnica ReAct para tarefas que exigem informação externa.
5. Explicar o modelo BDI e quando ele é (e não é) aplicável a prompts.
6. Avaliar criticamente prompts e saídas de IA usando rúbricas.
7. Produzir um projeto final que demonstre domínio prático dos conceitos.

---

## 3. Estrutura geral — 5 módulos, 12 aulas

| Módulo | Tema | Aulas | Arquivo de referência |
|---|---|---|---|
| **M1** | Fundamentos | Aula 1, 2, 3 | `prompt-engineering.md` |
| **M2** | Frameworks práticos | Aula 4, 5, 6 | `race.md`, `tag.md`, `care.md` |
| **M3** | Técnicas avançadas | Aula 7, 8 | `react.md`, `bdi.md` |
| **M4** | Avaliação | Aula 9, 10 | `rubrica.md` |
| **M5** | Projeto final | Aula 11, 12 | (síntese de todos) |

---

## Módulo 1 — Fundamentos do Prompt Engineering

### Aula 1 — O que é prompt engineering e por que importa

**Objetivo de aprendizagem:** Definir prompt engineering e reconhecer seu papel na obtenção de respostas úteis de LLMs.

**Conteúdo:**
- Definição formal (M(p) → y ≈ y*)
- Princípio: o modelo é probabilístico, não determinístico
- Diferença entre "perguntar à IA" e "engenharia de prompt"
- Por que é mistura de arte e ciência

**Referência:** `prompt-engineering.md` seções 1-2.

**Exercício:** Reformular um prompt vago ("fale sobre IA") em prompt claro e específico.

---

### Aula 2 — Anatomia de um prompt profissional

**Objetivo de aprendizagem:** Identificar as 5 seções padrão de um prompt bem estruturado.

**Conteúdo:**
- Identidade, Instruções, Exemplos, Contexto, Entrada
- Ordem recomendada das seções
- Uso de Markdown e tags XML para delimitar blocos
- A "regra de ouro": mostre a um colega sem contexto — se ele confundir, o modelo também confundirá

**Referência:** `prompt-engineering.md` seção 3; `care.md` seção 4.1 (Context).

**Exercício:** Decompor um prompt-exemplo dado nas 5 seções.

---

### Aula 3 — Técnicas estabelecidas

**Objetivo de aprendizagem:** Reconhecer e diferenciar 6 técnicas de prompt consolidadas.

**Conteúdo:**
- Zero-shot, Few-shot, Chain-of-thought, Role prompting, Structured output, Prompt chaining
- Quando usar cada uma
- Boas práticas de produção (versionar prompts, evals, snapshots de modelo)

**Referência:** `prompt-engineering.md` seções 4-5.

**Exercício:** Aplicar few-shot prompting para padronizar o formato de 3 respostas de IA.

---

## Módulo 2 — Frameworks Práticos de Prompt

### Aula 4 — Framework RACE

**Objetivo de aprendizagem:** Construir prompts completos usando RACE.

**Conteúdo:**
- Definição: Role · Action · Context · Expectation
- Características (complexidade baixa, custo de tokens baixo)
- Quando usar (escrita profissional, análise, Q&A, code review)
- Os 4 componentes explicados em detalhe
- 2 exemplos completos (explicação financeira; UX writing)

**Referência:** `race.md` completo.

**Exercício:** Construir um prompt RACE para uma tarefa do próprio trabalho do aluno.

---

### Aula 5 — Framework TAG

**Objetivo de aprendizagem:** Construir prompts rápidos e objetivos usando TAG.

**Conteúdo:**
- Definição: Task · Action · Goal
- O "prompt mínimo viável"
- Diferença crítica: Task (escopo) vs Action (método)
- Quando usar (draft rápido, tradução, copy de marketing, listas)
- Quando NÃO usar (tarefas complexas multi-etapas)
- Comparação RACE vs TAG

**Referência:** `tag.md` completo.

**Exercício:** Converter um prompt RACE da Aula 4 em prompt TAG e comparar resultados.

---

### Aula 6 — Framework CARE

**Objetivo de aprendizagem:** Construir prompts que exigem contexto rico e exemplo usando CARE (versão NN/G).

**Conteúdo:**
- Definição NN/G: Context · Ask · Rules · Examples
- Por que adotamos a versão da Nielsen Norman Group (autoridade principal)
- Variante concorrente (Context · Action · Result · Example) do Prompt Edit — registro didático
- Quando usar (comunicação empresarial, e-mails, propostas, UX writing)
- Limitações documentadas pela própria NN/G (dá trabalho, pode custar mais tempo que fazer manualmente)
- Exemplo completo de Kate Moran (mensagens de erro de login)

**Referência:** `care.md` completo.

**Exercício:** Construir um prompt CARE para um e-mail profissional real do aluno.

---

## Módulo 3 — Técnicas Avançadas

### Aula 7 — ReAct: raciocínio + ação

**Objetivo de aprendizagem:** Aplicar ReAct para tarefas que exigem informação externa.

**Conteúdo:**
- Definição (Yao et al., 2022, arXiv:2210.03629)
- Trajetória Thought → Action → Observation
- Motivação: CoT alucina; acting puro não raciocinha; ReAct combina
- Resultados empíricos (HotpotQA, Fever, ALFWorld, WebShop)
- Implementação prática com LangChain
- Limitações (depende da qualidade das buscas)

**Referência:** `react.md` completo.

**Exercício:** Escrever a trajetória Thought/Action/Observation para um problema que exija busca externa.

---

### Aula 8 — BDI: arquitetura de agentes (e sua analogia a prompts)

**Objetivo de aprendizagem:** Explicar o modelo BDI e usar sua lógica como analogia para prompts estruturados.

**Conteúdo:**
- Definição: Beliefs · Desires · Intentions (Bratman 1987; Rao & Georgeff 1995)
- BDI **não é framework de prompt** — é modelo de agentes de software
- Ciclo do interpretador BDI
- Implementações (PRS, Jason, JaCaMo)
- Aplicações reais em 2026 (robótica, cloud, MAS, integração com LLMs)
- Analogia cuidadosa: usar BDI para simular um agente com objetivos e tomada de decisão

**Referência:** `bdi.md` completo.

**Exercício:** Construir um prompt no formato BDI para um caso que exija "agente com estado interno" (ex.: assistente jurídico, planejador financeiro).

---

## Módulo 4 — Avaliação com Rúbricas

### Aula 9 — O que é uma rúbrica e como construí-la

**Objetivo de aprendizagem:** Definir rúbrica, identificar seus componentes e tipos.

**Conteúdo:**
- Definição (Popham 1997; Carnegie Mellon)
- Componentes: critérios, descritores, níveis de desempenho
- Tipos: holística, analítica, de desenvolvimento
- Benefícios para professor e aluno
- Método de 5 passos (Goodrich 1996)
- Quando usar e quando não usar

**Referência:** `rubrica.md` seções 1-7, 9-11.

**Exercício:** Construir uma rúbrica analítica simples (3 critérios × 4 níveis) para avaliar um texto qualquer.

---

### Aula 10 — Rúbricas para prompt engineering

**Objetivo de aprendizagem:** Aplicar rúbricas para avaliar prompts e saídas de IA.

**Conteúdo:**
- Por que rúbricas importam para prompt engineering (pontuação entre frameworks e avaliação objetiva)
- 3 usos: avaliar prompts dos alunos, avaliar saídas da IA, avaliar competência geral
- Rúbrica-exemplo para avaliar prompt RACE
- Rúbrica-exemplo para avaliar saída de IA generativa
- **Transparência:** estas rúbricas são construção didática, não validadas empiricamente
- Boas práticas (compartilhar antes da entrega, descritores observáveis, calibrar com outros avaliadores)

**Referência:** `rubrica.md` seção 8, 12.

**Exercício:** Aplicar a rúbrica de saída de IA a uma resposta gerada por um LLM e justificar a nota em cada critério.

---

## Módulo 5 — Projeto Final

### Aula 11 — Orientação do projeto final

**Objetivo de aprendizagem:** Compreender o escopo, etapas e critérios de avaliação do projeto final.

**Conteúdo:**
- Escopo do projeto (escolher um caso real, aplicar 2 frameworks, avaliar com rúbrica)
- Entregáveis (3 prompts + 3 saídas + relatório de avaliação)
- Cronograma sugerido (2 semanas)
- Rúbrica de correção (explicada em detalhe)

**Referência:** `projeto-final.md`.

**Exercício:** Submeter a proposta de caso para aprovação do instrutor.

---

### Aula 12 — Defesa e encerramento

**Objetivo de aprendizagem:** Defender o projeto e receber feedback estruturado.

**Conteúdo:**
- Apresentação do projeto (5 min por aluno)
- Feedback estruturado pela rúbrica
- Encerramento: próximos passos de aprendizagem contínua
- Como manter-se atualizado (acompanhar documentações oficiais)

**Referência:** `projeto-final.md` (rúbrica final).

---

## 4. Materiais de apoio

| Material | Arquivo | Uso |
|---|---|---|
| Documentação base | `docs/*.md` | Leitura obrigatória complementar às videoaulas |
| Exercícios | `exercicios.md` | Aplicação prática por aula |
| Roteiros de gravação | `roteiro-aulas.md` | Apoio à produção das videoaulas |
| Projeto final | `projeto-final.md` | Avaliação final |
| Rúbricas | `rubrica.md` (seção 8) | Correção de exercícios e projeto |

---

## 5. Avaliação

| Componente | Peso |
|---|---|
| Exercícios das aulas 1-10 | 40% |
| Projeto final | 50% |
| Participação em fórum | 10% |

**Aprovação:** nota ≥ 7,0 (escala 0-10).

---

## 6. Recomendação para NotebookLM

Carregue como fontes no NotebookLM (após revisão final):
1. Os 7 arquivos em `docs/`
2. `exercicios.md`, `projeto-final.md`, `roteiro-aulas.md` (a serem criados)

Gere a partir daí:
- Guia de estudo por módulo
- FAQ do curso
- Resumos em áudio (Audio Overview) por módulo
- Quiz automático por aula

> ⚠️ NotebookLM fundamenta-se apenas nas fontes carregadas. Antes de carregar, revise cada arquivo para garantir que estão consistentes com o que você quer ensinar.

---

## 7. Observação de transparência acadêmica (para o instrutor)

| Componente | Status |
|---|---|
| Prompt engineering (geral) | ✅ Documentação oficial (OpenAI, Anthropic, DAIR.AI, Learn Prompting) |
| ReAct | ✅ Paper acadêmico peer-reviewed (Yao et al., 2022) |
| BDI | ✅ Modelo acadêmico formal (Bratman 1987; Rao & Georgeff 1995) |
| RACE, TAG | ⚠️ Heurísticas práticas — não acadêmicas. Apresentar como tal. |
| CARE | ⚠️ Heurística prática proposta pela NN/G (maior autoridade, mas não peer-reviewed) |
| Rúbricas (conceito) | ✅ Literatura acadêmica consolidada (Popham, Herman, Goodrich, Dawson) |
| Rúbricas para prompt engineering (seção 8 do rubrica.md) | ⚠️ Construção didática própria — não validada empiricamente |

> O curso deve deixar claro para os alunos quais conteúdos são **técnicas consolidadas** e quais são **heurísticas práticas**. Isso protege a credibilidade do curso e respeita o princípio de não inventar.