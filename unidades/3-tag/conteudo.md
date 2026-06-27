# Unidade 3 — Framework TAG

> Curso: Prompt Engineering na Prática
> Materiais: vídeo (8-10 min) + apresentação + infográfico
> Carga horária: 2h (vídeo + leitura + 2 exercícios)

---

## 1. Objetivos de aprendizagem

Ao final desta unidade, o aluno será capaz de:

1. **Definir** o framework TAG e seus 3 componentes.
2. **Diferenciar** Task (escopo) e Action (método) — a confusão mais comum.
3. **Escolher** quando TAG é mais adequado que RACE.
4. **Converter** um prompt RACE em TAG e comparar resultados.

---

## 2. Conteúdo

### 2.1 Definição

**TAG** é um framework minimalista de estruturação de prompts com três componentes focados — **Task, Action, Goal** — que reduzem a escrita do prompt ao essencial, permitindo obter resultados de alta qualidade da IA rapidamente, sem over-engineering.

| Letra | Componente | Significado |
|-------|------------|-------------|
| **T** | **Task** | Nomeie o que precisa ser feito (objetivo de alto nível). |
| **A** | **Action** | Dê a instrução específica (como executar, com verbos fortes). |
| **G** | **Goal** | Defina o que o sucesso parece (critérios de sucesso/aceitação). |

### 2.2 Características

| Atributo | Valor |
|---|---|
| Complexidade | Muito baixa — o prompt mínimo viável |
| Custo de tokens | Baixo |
| Indicado para | Pedidos rápidos e bem definidos |
| Nível | Iniciante |

> **TL;DR:** o componente **Goal** é o mais comumente pulado — **sempre o inclua** para evitar que a IA otimize para o alvo errado.

### 2.3 Os 3 componentes explicados

**T — Task (nomeie o que precisa ser feito):**
State o objetivo de alto nível em uma ou duas frases. Esta é a categoria do trabalho: *"escreva um subject line"*, *"traduza este parágrafo"*, *"gere uma lista de títulos de posts de blog"*. Task define o escopo e o tipo de saída esperado. Mantenha concreto e focado em substantivos.

**A — Action (dê a instrução específica):**
Action é onde você usa **verbos fortes e específicos** para dizer à IA exatamente como executar a tarefa. É aqui que vivem direção criativa, restrições e métodos: *"gere cinco opções que criem curiosidade"*, *"traduza preservando o tom casual"*, *"filtre por relevância para pequenos negócios"*. Quanto mais específica a Action, menos interpretação o modelo precisa fazer.

**G — Goal (defina os critérios de sucesso):**
Goal responde: **para que serve esta saída e o que a torna bem-sucedida?** Inclua o público-alvo, a plataforma ou caso de uso e quaisquer critérios mensuráveis de qualidade (menos de 50 caracteres, pronto para publicar, adequado para leitor não técnico). Goal evita que a IA otimize para um alvo diferente daquele que você realmente quer.

### 2.4 Diferença crítica: Task vs Action

| Componente | Foco | Exemplo |
|---|---|---|
| **Task** | Objetivo de alto nível — categoria do que precisa ser feito | *"escreva um subject line"*, *"traduza um documento"* |
| **Action** | Instrução operacional específica — descrição verbo-dirigida de como executar | *"gere cinco opções que criem urgência"*, *"traduza preservando o tom casual"* |

> **Task define escopo; Action define método.** Esta é a distinção que mais confunde iniciantes.

### 2.5 Quando usar o TAG

| Caso de uso | Aplicação |
|---|---|
| **Draft rápido** | E-mail, resumo, lista de ideias — contexto já está claro pelo assunto |
| **Tradução** | O que traduzir (Task), restrições de tom (Action), público-alvo (Goal) |
| **Copy de marketing** | Tipo de copy (Task), direção criativa (Action), objetivo de conversão (Goal) |
| **Geração de listas** | Peça lista (Task), como gerá-las/filtrá-las (Action), propósito (Goal) |
| **Reformatação** | Conteúdo-fonte e formato alvo (Task), regras de transformação (Action), uso (Goal) |
| **Refinamento iterativo** | Tarefa de revisão (Task), método de melhoria (Action), padrão alvo (Goal) |

### 2.6 Quando NÃO usar o TAG

- **Fluxos multi-etapas complexos** → use RISE
- **Tarefas que exigem persona detalhada** → use ROLE ou RACE
- **Estratégia ou planejamento** → onde contexto completo importa, use COAST ou RACE

### 2.7 Prós e contras

| 🟢 Prós | 🔴 Contras |
|---|---|
| Framework estruturado mais rápido de escrever — 3 seções curtas | Sem componente Role — respostas podem carecer do tom de especialista |
| Fácil de lembrar e aplicar sem notas | Sem slot dedicado Context para informações de fundo nuanceadas |
| Escala bem para tarefas repetitivas e templadas | Menos eficaz para tarefas complexas, multi-etapas ou criativas |
| Bom framework de entrada para iniciantes | — |

### 2.8 Exemplos práticos

#### Exemplo 1 — Subject lines de campanha de reengajamento

> **Task:** Escreva um subject line para uma campanha de e-mail de reengajamento.
>
> **Action:** Gere cinco opções de subject line que criem curiosidade e senso de urgência sem ser clickbait.
>
> **Goal:** Aumentar as taxas de abertura entre assinantes que não abriram um e-mail nos últimos 90 dias. Cada subject line deve ter menos de 50 caracteres e funcionar bem em mobile.

#### Exemplo 2 — Tradução de descrição de produto

> **Task:** Traduza a descrição de produto a seguir do inglês para o francês.
>
> **Action:** Traduza com precisão preservando a voz da marca casual e amigável. Não use construções francesas excessivamente formais.
>
> **Goal:** Uma descrição de produto em francês pronta para publicar em nosso e-commerce direcionado a clientes francófonos da França e Bélgica.
>
> ---
> Texto original:
> *"Meet Spark — the portable Bluetooth speaker that goes wherever you do. Waterproof, drop-proof, and loud enough to fill any room."*

### 2.9 Comparação com frameworks relacionados

| Framework | Componentes | Diferença em relação ao TAG |
|---|---|---|
| **APE** | Action, Purpose, Expectation | APE foca em quê (Action), por que/para quem (Purpose) e qualidade (Expectation). TAG é mais orientado à tarefa. |
| **RACE** | Role, Action, Context, Expectation | RACE adiciona Role e Context para saídas mais ricas |
| **RTF** | Role, Task, Format | RTF adiciona persona (Role) ao invés de Goal explícito |

---

## 3. Exercícios da unidade

### Exercício 3.1 — Converter RACE para TAG (guiado)
Converta o prompt RACE do exercício 2.1 (e-mail de follow-up) em prompt TAG, mantendo apenas o essencial. Compare as saídas. **Gabarito no `exercicios.md`.**

### Exercício 3.2 — TAG para tradução + headlines (livre)
Aplique TAG a uma tarefa de tradução (EN → PT-BR) e a uma tarefa de geração de 10 headlines para um post de LinkedIn sobre IA. Entregue os dois prompts e as saídas.

---

## 4. Leitura complementar

- `docs/tag.md` — documento base completo com FAQ detalhado

---

## 5. Fontes verificadas

1. **Prompt Edit** — TAG Framework: https://www.promptedit.app/prompt-framework/tag
2. **PromptVibe** — TAG Prompt Framework: https://www.promptvibe.co/frameworks/tag-prompt-framework
3. **Easy AI Beginner** — TAG Framework for ChatGPT: https://easyaibeginner.com/tag-framework-for-chatgpt/

> **Transparência:** 3 fontes convergem para a mesma definição. TAG é uma **heurística prática mnemônica**, sem paper acadêmico original. Compatível com as técnicas estabelecidas documentadas pelas fontes oficiais.