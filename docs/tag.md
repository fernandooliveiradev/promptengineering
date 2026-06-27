# Framework TAG

> **T**ask · **A**ction · **G**oal
> Documentação de apoio para cursos online.

---

## 1. Definição

O **TAG** é um *framework* minimalista de estruturação de prompts com três componentes focados — **Task, Action, Goal** — que reduzem a escrita do prompt ao essencial, permitindo obter resultados de alta qualidade da IA rapidamente, sem *over-engineering*.

| Letra | Componente | Significado |
|-------|------------|-------------|
| **T** | **Task** | Nomeie o que precisa ser feito (objetivo de alto nível). |
| **A** | **Action** | Dê a instrução específica (como executar, com verbos fortes). |
| **G** | **Goal** | Defina o que o sucesso parece (critérios de sucesso/aceitação). |

---

## 2. Objetivo

O TAG é o **prompt mínimo viável** (*minimal viable prompt*) — três componentes focados que respondem:
- **O que** precisa ser feito (Task);
- **Como** deve ser feito (Action);
- **Como é o sucesso** (Goal).

É intencionalmente enxuto. Onde frameworks como **RACE** ou **RISEN** adicionam componentes para persona, contexto, exemplos e estilo, o TAG reduz tudo ao menor conjunto de instruções que ainda produz resultados confiáveis e no alvo. É perfeito para situações em que você conhece bem a tarefa, o contexto é evidente e a velocidade importa mais do que controle fino.

> **Pense no TAG como** o template de prompt *quick-start* que você alcança quando tem um trabalho claro a fazer e não quer passar dois minutos compondo um brief estruturado. É um ótimo primeiro framework para aprender e um *fallback* útil mesmo para engenheiros de prompt experientes que precisam de uma resposta rápida.

---

## 3. Características

| Atributo | Valor |
|---|---|
| Complexidade | Muito baixa — o prompt mínimo viável |
| Custo de tokens | Baixo |
| Indicado para | Pedidos rápidos e bem definidos |
| Nível | Iniciante |

> **TL;DR:** o componente **Goal** é o mais comumente pulado — **sempre o inclua** para evitar que a IA otimize para o alvo errado.

---

## 4. Quando usar o TAG

| Caso de uso | Aplicação |
|---|---|
| **Draft rápido** | Quando você precisa de um primeiro rascunho rapidamente — e-mail, resumo, lista de ideias — e o contexto já está claro pelo próprio assunto. |
| **Tarefas de tradução** | Especifique o que traduzir (Task), restrições de tom/estilo (Action) e o público-alvo ou contexto de publicação (Goal) para texto traduzido pronto para publicar. |
| **Copy de marketing** | Defina o tipo de copy (Task), dê direção criativa como tom, limite de palavras ou dispositivo (Action) e state o objetivo de conversão/engajamento (Goal). |
| **Geração de listas** | Peça uma lista de ideias/opções/itens (Task), especifique como gerá-las ou filtrá-las (Action) e state o propósito que elas servirão (Goal). |
| **Reformatação de conteúdo** | Descreva o conteúdo-fonte e o formato alvo (Task), as regras de transformação (Action) e como o conteúdo reformulado será usado (Goal). |
| **Refinamento iterativo** | Quando você tem um rascunho existente e precisa melhorias direcionadas — use TAG para especificar a tarefa de revisão, o método de melhoria e o padrão de qualidade alvo. |

---

## 5. Como usar — os três componentes

### 5.1 Task — Nomeie o que precisa ser feito
State o objetivo de alto nível em uma ou duas frases. Esta é a categoria do trabalho: *"escreva um subject line"*, *"traduza este parágrafo"*, *"gere uma lista de títulos de posts de blog"*. Task define o escopo e o tipo de saída esperado. Mantenha concreto e focado em substantivos.

### 5.2 Action — Dê a instrução específica
Action é onde você usa **verbos fortes e específicos** para dizer à IA exatamente como executar a tarefa. É aqui que vivem direção criativa, restrições e métodos: *"gere cinco opções que criem curiosidade"*, *"traduza preservando o tom casual"*, *"filtre por relevância para pequenos negócios"*. Quanto mais específica a Action, menos interpretação o modelo precisa fazer.

### 5.3 Goal — Defina os critérios de sucesso
Goal responde: **para que serve esta saída e o que a torna bem-sucedida?** Inclua o público-alvo, a plataforma ou caso de uso e quaisquer critérios mensuráveis de qualidade (menos de 50 caracteres, pronto para publicar, adequado para leitor não técnico). Goal evita que a IA otimize para um alvo diferente daquele que você realmente quer.

---

## 6. Exemplos práticos

### Exemplo 1 — Subject lines de campanha de reengajamento

> **Task:** Escreva um subject line para uma campanha de e-mail de reengajamento.
>
> **Action:** Gere cinco opções de subject line que criem curiosidade e senso de urgência sem ser clickbait.
>
> **Goal:** Aumentar as taxas de abertura entre assinantes que não abriram um e-mail nos últimos 90 dias. Cada subject line deve ter menos de 50 caracteres e funcionar bem em mobile.

### Exemplo 2 — Tradução de descrição de produto

> **Task:** Traduza a descrição de produto a seguir do inglês para o francês.
>
> **Action:** Traduza com precisão preservando a voz da marca casual e amigável. Não use construções francesas excessivamente formais.
>
> **Goal:** Uma descrição de produto em francês pronta para publicar em nosso e-commerce direcionado a clientes francófonos da França e Bélgica.
>
> ---
> Texto original:
> *"Meet Spark — the portable Bluetooth speaker that goes wherever you do. Waterproof, drop-proof, and loud enough to fill any room."*

---

## 7. Prós e contras

| 🟢 Prós | 🔴 Contras |
|---|---|
| Framework estruturado mais rápido de escrever — três seções curtas | Sem componente Role — respostas podem carecer do tom de especialista |
| Fácil de lembrar e aplicar sem notas | Sem slot dedicado Context para informações de fundo nuanceadas |
| Escala bem para tarefas repetitivas e templadas | Menos eficaz para tarefas complexas, multi-etapas ou criativas |
| Bom framework de entrada para iniciantes | — |

---

## 8. Comparação com frameworks relacionados

| Framework | Componentes | Diferença em relação ao TAG |
|---|---|---|
| **APE** | Action, Purpose, Expectation | APE foca no quê (Action), por que/para quem (Purpose) e qualidade da saída (Expectation). TAG é mais orientado a tarefa e focado na saída; APE constrói consciência de audiência mais explicitamente via Purpose. |
| **RACE** | Role, Action, Context, Expectation | RACE adiciona Role e Context para saídas mais ricas |
| **RTF** | Role, Task, Format | RTF adiciona persona (Role) ao invés de Goal explícito |
| **Zero-shot** | (nenhum) | Sem estrutura — compare a diferença |

---

## 9. Diferença entre Task e Action (esclarecimento comum)

| Componente | Foco | Exemplo |
|---|---|---|
| **Task** | Objetivo de alto nível — categoria do que precisa ser feito | *"escreva um subject line"*, *"traduza um documento"* |
| **Action** | Instrução operacional específica — descrição verbo-dirigida de como executar | *"gere cinco opções que criem urgência"*, *"traduza preservando o tom casual"* |

**Task define escopo; Action define método.**

---

## 10. FAQ essencial

**Devo adicionar contexto embora TAG não tenha slot dedicado?**
Sim. TAG é um framework mínimo, não restritivo. Você pode (e frequentemente deve) adicionar uma frase breve de contexto dentro da sua descrição de Task ou Action. Para tarefas complexas, considere atualizar para RACE ou CARE, que têm slots de Context dedicados. TAG é o ponto de partida; adapte conforme necessário.

**TAG serve para escrita criativa?**
Sim. Defina Task como o tipo de saída criativa (conto, poema, tagline), Action como a direção criativa específica (escreva ao estilo noir, use monólogo interno, rime em ABAB) e Goal como o propósito ou público (engajar leitores de 18-25, definir tom melancólico). Tarefas criativas se beneficiam de um Goal claro para ancorar as escolhas da IA.

---

## 11. Referências (verificadas)

1. **Prompt Edit** — *TAG Framework for Prompt Engineering*. https://www.promptedit.app/prompt-framework/tag — Acessado em: jun/2026. Site mantido por Sebastian Messingfeld (Cologne, Alemanha).
2. **PromptVibe** — *TAG Prompt Framework — Task, Action, Goal*. https://www.promptvibe.co/frameworks/tag-prompt-framework — Acessado em: jun/2026. Confirma definição TAG = Task, Action, Goal, com exemplos para código e copy de marketing.
3. **Easy AI Beginner** — *TAG Framework for ChatGPT Prompt Engineering (Task Action Goal)*. https://easyaibeginner.com/tag-framework-for-chatgpt/ — Acessado em: jun/2026 (referência terciária confirmada via DuckDuckGo).

> Nota: as três fontes convergem para a mesma definição: **TAG = Task, Action, Goal**, framework minimalista de 3 componentes para tarefas diretas e bem definidas.

---

## 12. Observação metodológica

O TAG é uma **heurística prática mnemônica** de organização de prompts, catalogada em múltiplas ferramentas especializadas (Prompt Edit, PromptVibe, Easy AI Beginner). **Não há um *paper* acadêmico original que o formalize**; trata-se de uma **técnica prática derivada das melhores práticas de prompt engineering**.

Mesmo sem origem acadêmica formal, o TAG é **compatível com as técnicas estabelecidas** (instrução explícita, critérios de sucesso claros) documentadas nas fontes oficiais — OpenAI, Anthropic, DAIR.AI e Learn Prompting. Sua filosofia de "prompt mínimo viável" alinha-se à recomendação da Anthropic de ser claro e direto, evitando prompts desnecessariamente longos para tarefas simples.