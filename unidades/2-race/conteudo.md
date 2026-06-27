# Unidade 2 — Framework RACE

> Curso: Prompt Engineering na Prática
> Materiais: vídeo (8-10 min) + apresentação + infográfico
> Carga horária: 2h (vídeo + leitura + 2 exercícios)

---

## 1. Objetivos de aprendizagem

Ao final desta unidade, o aluno será capaz de:

1. **Definir** o framework RACE e seus 4 componentes.
2. **Construir** prompts completos usando RACE.
3. **Escolher** quando RACE é mais adequado que prompts não-estruturados.
4. **Avaliar** criticamente um prompt RACE identificando componentes faltantes.

---

## 2. Conteúdo

### 2.1 Definição

**RACE** é um framework de estruturação de prompts com quatro componentes memoráveis:

| Letra | Componente | Significado |
|-------|------------|-------------|
| **R** | **Role** | Define a persona/perfil especialista que a IA deve assumir. |
| **A** | **Action** | State exatamente o que a IA deve fazer, com verbo ativo. |
| **C** | **Context** | Fornece o contexto/informações de fundo necessárias. |
| **E** | **Expectation** | Especifica o formato, tom, extensão e critérios da saída. |

### 2.2 Características

| Atributo | Valor |
|---|---|
| Complexidade | Baixa — fácil de memorizar e aplicar |
| Custo de tokens | Baixo |
| Indicado para | Escrita profissional, análise, Q&A, code review |
| Nível | Iniciante |

### 2.3 Os 4 componentes explicados

**R — Role (persona especialista):**
Diga à IA **quem ela deve ser**. Seja específico: *"Você é um UX designer sênior com 10 anos de experiência em mobile"* produz resultados muito melhores que *"Você é um designer"*. Inclua domínio, senioridade e especialização relevante. Uma Role bem feita prepara o modelo para usar vocabulário, suposições e abordagem corretos.

**A — Action (ação específica):**
Use um **verbo ativo claro**: escreva, resuma, compare, depure, traduza, reescreva, explique, redija, gere. Siga o verbo com o objeto específico. Evite linguagem vaga como *"me ajude com"* ou *"fale sobre"*. Quanto mais precisa a Action, menos o modelo precisa adivinhar.

**C — Context (contexto de fundo):**
Contexto é o componente **mais frequentemente pulado** e o maior responsável por saídas genéricas. Inclua: quem é o público, quais restrições se aplicam, qual é a situação existente e quais fatos específicos do domínio a IA precisa conhecer. Um bom contexto transforma uma resposta genérica em uma resposta adaptada e consciente da situação.

**E — Expectation (expectativa de saída):**
Diga à IA exatamente como é uma **resposta bem-sucedida**: formato (lista numerada, tabela markdown, parágrafos), extensão (contagem de palavras, número de itens), tom (formal, conversacional, técnico) e restrições rígidas (sem jargão, inclua CTA, até 150 palavras). Esse é o componente que **mais diretamente controla a qualidade da saída**.

### 2.4 Quando usar o RACE

| Caso de uso | Aplicação |
|---|---|
| **Escrita de conteúdo** | Persona de escritor + tipo de conteúdo + contexto do público + tom/extensão |
| **E-mails profissionais** | Role = comunicador + Action = redigir/reescritor + Context = relação e propósito + Expectation = extensão e formalidade |
| **Resumos de pesquisa** | Role = analista + Action = resumir + Context = material-fonte + Expectation = formato (bullets, brief) |
| **Revisão/geração de código** | Role = dev sênior + Action = ação de código + Context = linguagem/framework + Expectation = comentários, estilo |
| **Explicações educacionais** | Role = professor + Action = explicar + Context = nível do aprendiz + Expectation = analogias/exemplos |

### 2.5 Prós e contras

| 🟢 Prós | 🔴 Contras |
|---|---|
| Fácil de memorizar — 4 componentes intuitivos | Sem slot dedicado para exemplos — adicione-os manualmente quando necessário |
| Cobre o essencial sem complexidade | Menos preciso que RISEN ou CRISPE para tarefas nuanceadas |
| Funciona em praticamente qualquer domínio | Expectation requer prática para ser bem escrito |
| Saídas significativamente melhores que prompts não estruturados | — |

### 2.6 Exemplos práticos

#### Exemplo 1 — Explicação financeira para iniciantes

> **Role:** Você é um consultor financeiro sênior com 20 anos de experiência em finanças pessoais e planejamento de investimentos.
>
> **Action:** Escreva uma explicação em linguagem simples de como funciona o juros compostos e por que começar cedo importa.
>
> **Context:** Meu público é recém-formados universitários que nunca investiram e estão intimidados por jargão financeiro. Têm cerca de US$ 200–500/mês para investir.
>
> **Expectation:** Produza uma explicação de 300 palavras com um exemplo numérico concreto mostrando a diferença entre começar aos 22 vs. 32. Use linguagem encorajadora, sem jargão.

#### Exemplo 2 — UX Writing: reescrita de mensagem de erro

> **Role:** Você é um UX writer experiente especializado em onboarding de apps mobile.
>
> **Action:** Reescreva a seguinte mensagem de erro para torná-la mais clara e amigável: *"Error 403: Access denied. Insufficient privileges."*
>
> **Context:** Esta mensagem aparece em um app de fitness quando um usuário free tenta acessar um recurso premium. A voz da marca é calorosa, motivadora e conversacional.
>
> **Expectation:** Forneça três opções alternativas, cada uma com menos de 20 palavras, que expliquem o que aconteceu e direcionem o usuário ao upgrade — sem parecer insistente.

### 2.7 Comparação com frameworks relacionados

| Framework | Componentes | Diferença em relação ao RACE |
|---|---|---|
| **RTF** | Role, Task, Format | RACE expande RTF adicionando Action (verbo) e Context dedicado |
| **RISEN** | Role, Instructions, Steps, Examples, Narrowing | RISEN adiciona Instructions e Narrowing; mais fino, porém mais lento |
| **CRISPE** | Capacity, Role, Insight, Statement, Personality, Experiment | CRISPE adiciona Style e Examples; seis partes |
| **APE** | Action, Purpose, Expectation | APE tem Purpose (audiência); não tem Role explícita |

---

## 3. Exercícios da unidade

### Exercício 2.1 — RACE para e-mail de follow-up (guiado)
Construa um prompt RACE completo para "escrever um e-mail de follow-up após uma entrevista de emprego". **Gabarito no `exercicios.md`.**

### Exercício 2.2 — RACE para tarefa própria (livre)
Construa um prompt RACE para uma tarefa real do seu trabalho. Entregue: prompt + saída obtida + autoavaliação em 1 parágrafo.

---

## 4. Leitura complementar

- `docs/race.md` — documento base completo com 2 exemplos extras e comparação detalhada

---

## 5. Fontes verificadas

1. **Prompt Edit** — RACE Framework: https://www.promptedit.app/prompt-framework/race — Acessado em: jun/2026. Site mantido por Sebastian Messingfeld (Cologne, Alemanha).

> **Transparência:** RACE é uma **heurística prática mnemônica**, sem paper acadêmico original. É compatível com as técnicas estabelecidas (role prompting, structured output) documentadas pelas fontes oficiais.