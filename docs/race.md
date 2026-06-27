# Framework RACE

> **R**ole · **A**ction · **C**ontext · **E**xpectation
> Documentação de apoio para cursos online.

---

## 1. Definição

O **RACE** é um *framework* de estruturação de prompts com quatro componentes memoráveis — **Role, Action, Context, Expectation** — que transformam pedidos vagos em prompts precisos e de alta qualidade em menos de dois minutos.

| Letra | Componente | Significado |
|-------|------------|-------------|
| **R** | **Role** | Define a persona/perfil especialista que a IA deve assumir. |
| **A** | **Action** | State exatamente o que a IA deve fazer, com verbo ativo. |
| **C** | **Context** | Fornece o contexto/informações de fundo necessárias. |
| **E** | **Expectation** | Especifica o formato, tom, extensão e critérios da saída. |

---

## 2. Objetivo

O RACE é um *framework* **versátil de quatro componentes** que cobre as variáveis de prompt mais impactantes — **persona especialista, tarefa específica, contexto de fundo e formato de saída** — em uma estrutura memorável e aprendível.

É indicado como **template de uso geral** para tarefas de escrita profissional, análise e geração de conteúdo de qualquer complexidade, sendo uma boa opção para **padronizar prompts em equipes**, pois seus quatro componentes são não sobrepostos e intuitivos para usuários não técnicos.

---

## 3. Características

| Atributo | Valor |
|---|---|
| Complexidade | Baixa — fácil de memorizar e aplicar |
| Custo de tokens | Baixo |
| Indicado para | Escrita cotidiana, análise e tarefas de Q&A |
| Nível | Iniciante |

---

## 4. Quando usar o RACE

| Caso de uso | Aplicação |
|---|---|
| **Escrita de conteúdo** | Atribua uma persona de escritor, especifique o tipo de conteúdo e mensagens-chave, forneça o contexto do público e defina tom e contagem de palavras. |
| **E-mails profissionais** | Defina Role como comunicador, Action como redigir/reescrever o e-mail, Context como a relação e o propósito, e Expectation como extensão e formalidade. |
| **Resumos de pesquisa** | Dê à IA um papel de analista, peça para resumir um tópico, forneça o material-fonte em Context e especifique o formato (bullets, brief executivo etc.). |
| **Revisão e geração de código** | Atribua o papel de desenvolvedor sênior, especifique a ação de código, forneça linguagem/framework em Context e defina expectativas de comentários, estilo e profundidade. |
| **Explicações educacionais** | Configure a IA como professor, peça para explicar um conceito, descreva o nível do aprendiz em Context e especifique analogias, exemplos ou formato de aula. |
| **Narrativas de análise de dados** | Atribua o papel de analista de dados, peça interpretação dos achados, forneça o conjunto de dados em Context e espere uma narrativa com conclusões para público não técnico. |

---

## 5. Como usar — os quatro componentes

### 5.1 Role — Defina a persona especialista
Diga à IA **quem ela deve ser**. Seja específico: *"Você é um UX designer sênior com 10 anos de experiência em mobile"* produz resultados muito melhores que *"Você é um designer"*. Inclua domínio, senioridade e especialização relevante. Uma Role bem feita prepara o modelo para usar vocabulário, suposições e abordagem corretos.

### 5.2 Action — State exatamente o que fazer
Use um **verbo ativo claro**: escreva, resuma, compare, depure, traduza, reescreva, explique, redija, gere. Siga o verbo com o objeto específico. Evite linguagem vaga como *"me ajude com"* ou *"fale sobre"*. Quanto mais precisa a Action, menos o modelo precisa adivinhar.

### 5.3 Context — Forneça o contexto
Contexto é o componente **mais frequentemente pulado** e o maior responsável por saídas genéricas. Inclua: quem é o público, quais restrições se aplicam, qual é a situação existente e quais fatos específicos do domínio a IA precisa conhecer. Um bom contexto transforma uma resposta genérica em uma resposta adaptada e consciente da situação.

### 5.4 Expectation — Especifique a saída
Diga à IA exatamente como é uma **resposta bem-sucedida**: formato (lista numerada, tabela markdown, parágrafos), extensão (contagem de palavras, número de itens), tom (formal, conversacional, técnico) e restrições rígidas (sem jargão, inclua CTA, até 150 palavras). Esse é o componente que **mais diretamente controla a qualidade da saída**.

---

## 6. Exemplos práticos

### Exemplo 1 — Explicação financeira para iniciantes

> **Role:** Você é um consultor financeiro sênior com 20 anos de experiência em finanças pessoais e planejamento de investimentos.
>
> **Action:** Escreva uma explicação em linguagem simples de como funciona o juros compostos e por que começar cedo importa.
>
> **Context:** Meu público é recém-formados universitários que nunca investiram e estão intimidados por jargão financeiro. Têm cerca de US$ 200–500/mês para investir.
>
> **Expectation:** Produza uma explicação de 300 palavras com um exemplo numérico concreto mostrando a diferença entre começar aos 22 vs. 32. Use linguagem encorajadora, sem jargão.

### Exemplo 2 — UX Writing: reescrita de mensagem de erro

> **Role:** Você é um UX writer experiente especializado em onboarding de apps mobile.
>
> **Action:** Reescreva a seguinte mensagem de erro para torná-la mais clara e amigável: *"Error 403: Access denied. Insufficient privileges."*
>
> **Context:** Esta mensagem aparece em um app de fitness quando um usuário free tenta acessar um recurso premium. A voz da marca é calorosa, motivadora e conversacional.
>
> **Expectation:** Forneça três opções alternativas, cada uma com menos de 20 palavras, que expliquem o que aconteceu e direcionem o usuário ao upgrade — sem parecer insistente.

---

## 7. Prós e contras

| 🟢 Prós | 🔴 Contras |
|---|---|
| Fácil de memorizar — quatro componentes intuitivos | Sem slot dedicado para exemplos — adicione-os manualmente quando necessário |
| Cobre o essencial sem complexidade desnecessária | Menos preciso que RISEN ou CRISPE para tarefas muito nuanceadas |
| Funciona em praticamente qualquer tipo de tarefa/domínio | O componente Expectation requer alguma prática para ser bem escrito |
| Saídas significativamente melhores que prompts não estruturados | — |

---

## 8. Comparação com frameworks relacionados

| Framework | Componentes | Diferença em relação ao RACE |
|---|---|---|
| **RTF** | Role, Task, Format | RACE expande RTF adicionando Action (verbo) e Context dedicado |
| **RISEN** | Role, Instructions, Steps, Examples, Narrowing | RISEN adiciona Instructions e Narrowing; mais fino, porém mais lento |
| **CRISPE** | Capacity, Role, Insight, Statement, Personality, Experiment | CRISPE adiciona Style e Examples; seis partes |
| **APE** | Action, Purpose, Expectation | APE tem Purpose (audiência); não tem Role explícita |

---

## 9. Referências (verificadas)

1. **Prompt Edit** — *RACE Framework for Prompt Engineering*. https://www.promptedit.app/prompt-framework/race — Acessado em: jun/2026. Site mantido por Sebastian Messingfeld (Cologne, Alemanha), que cataloga 50+ frameworks de prompt.

---

## 10. Observação metodológica

O RACE é uma **heurística prática mnemônica** de organização de prompts, difundida em materiais de ensino e ferramentas especializadas (como o site Prompt Edit, que cataloga dezenas de frameworks semelhantes: RTF, RISEN, CRISPE, APE, BAB, CARE, TAG etc.). **Não há um *paper* acadêmico original que o formalize**; trata-se de uma **técnica prática derivada das melhores práticas de prompt engineering**.

Mesmo não tendo origem acadêmica formal, o RACE é **compatível com as técnicas estabelecidas** (role prompting, structured output, few-shot) documentadas nas fontes oficiais — OpenAI, Anthropic, DAIR.AI e Learn Prompting. Seus quatro componentes (persona, ação, contexto, expectativa) mapeiam diretamente para as seções recomendadas em um prompt profissional.