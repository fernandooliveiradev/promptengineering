# Unidade 1 — Fundamentos do Prompt Engineering

> Curso: Prompt Engineering na Prática
> Materiais desta unidade: vídeo (8-12 min) + apresentação + infográfico
> Carga horária: 3h (vídeo + leitura + 3 exercícios)

---

## 1. Objetivos de aprendizagem

Ao final desta unidade, o aluno será capaz de:

1. **Definir** prompt engineering e explicar por que é mistura de arte e ciência.
2. **Decompor** um prompt profissional nas 5 seções padrão (Identidade, Instruções, Exemplos, Contexto, Entrada).
3. **Reconhecer e diferenciar** 6 técnicas estabelecidas (zero-shot, few-shot, chain-of-thought, role prompting, structured output, prompt chaining).
4. **Reformular** prompts vagos em prompts claros e específicos.

---

## 2. Conteúdo por aula

### Aula 1.1 — O que é prompt engineering e por que importa

**Definição formal:**
Prompt Engineering (Engenharia de Prompts) é a disciplina que estuda como **estruturar instruções (prompts)** para modelos de linguagem (LLMs) de modo a obter respostas **consistentes, precisas e úteis**.

Dado um modelo \( M \) e um prompt \( p \), buscamos:

\[
M(p) \rightarrow y \quad \text{tal que} \quad y \approx y^*
\]

onde \( y^* \) é a resposta ideal. O papel do engenheiro de prompts é projetar \( p \) para maximizar a probabilidade de \( y \approx y^* \).

**Por que é arte + ciência:**
O modelo é **probabilístico** (não determinístico) — não há prompt perfeito, há prompts melhores e piores.

**Antes vs depois (exemplo):**
- ❌ Vago: "fale sobre ia"
- ✅ Específico: "Explique IA para um leigo em 200 palavras, use uma analogia do cotidiano, termine com um exemplo prático que o leitor já tenha usado."

**3 razões para aprender agora:**
1. IA generativa já é ferramenta de trabalho.
2. A diferença entre usuário comum e quem sabe prompt engineering é ~10x em produtividade.
3. É habilidade transferível — funciona com GPT, Claude, Gemini.

---

### Aula 1.2 — Anatomia de um prompt profissional

Um prompt profissional tipicamente tem **5 seções**, nessa ordem:

| Seção | Função | Exemplo |
|---|---|---|
| **Identidade** | Define a persona | "Você é um revisor de texto experiente em PT-BR." |
| **Instruções** | O que fazer (e o que NÃO fazer) | "Revise, corrija erros. Não reescreva o texto inteiro." |
| **Exemplos** | 3-5 entradas/saídas (few-shot) | "Se disser 'nós vai', sugira 'nós vamos'." |
| **Contexto** | Dados de fundo | "Texto para blog corporativo de RH, tom profissional." |
| **Entrada** | A tarefa específica deste turno | "Texto para revisão: 'A equipe nós vai...'" |

**Regra de ouro:** Mostre seu prompt a um colega sem contexto. Se ele confundir, o modelo também confundirá.

**Dica prática:** Use Markdown (cabeçalhos, listas) e tags XML para delimitar blocos.

---

### Aula 1.3 — Técnicas estabelecidas

| Técnica | O que é | Quando usar |
|---|---|---|
| **Zero-shot** | Instrução direta, sem exemplos | Tarefas comuns que o modelo já entende |
| **Few-shot** | 3-5 exemplos entrada-saída | Padronizar formato, tom, estilo |
| **Chain-of-thought (CoT)** | Pedir para pensar passo a passo | Matemática, lógica, raciocínio |
| **Role prompting** | Atribuir persona | Focar domínio e tom |
| **Structured output** | Pedir JSON | Quando a saída vai para código |
| **Prompt chaining** | Dividir tarefa em chamadas sequenciais | Tarefas complexas multi-etapas |

**Exemplo CoT (problema clássico):**
> *"Se 5 máquinas fazem 5 peças em 5 minutos, quantas peças 100 máquinas fazem em 100 minutos?"*

- Sem CoT: o modelo frequentemente erra ("100").
- Com CoT ("pense passo a passo"): acerta (2000).

**Boas práticas de produção:**
- Versionar prompts no código-fonte
- Criar suites de avaliação (evals)
- Fixar snapshots de modelo em produção
- Especificar formato de forma positiva ("responda em parágrafos") em vez de negativa ("não use markdown")

---

## 3. Exercícios da unidade

### Exercício 1.1 — Reformular prompt vago (guiado)
Reformule "fale sobre ia" em um prompt claro e específico. **Gabarito no `exercicios.md`.**

### Exercício 1.2 — Reformular prompt próprio (livre)
Escolha um prompt vago que você já usou e o reformule aplicando clareza, especificidade e contexto.

### Exercício 1.3 — Decompor nas 5 seções (guiado)
Decomponha um prompt-exemplo dado nas 5 seções (Identidade, Instruções, Exemplos, Contexto, Entrada).

### Exercício 1.4 — Few-shot classificação (guiado)
Aplique few-shot prompting para classificar sentimento no formato `sentimento: [...] — confiança: [...]%`.

### Exercício 1.5 — CoT problema matemático (livre)
Aplique chain-of-thought ao problema das máquinas/peças e compare com e sem CoT.

---

## 4. Leitura complementar

- `docs/prompt-engineering.md` — documento base completo
- `docs/care.md` seção 4.1 (Context)

---

## 5. Fontes verificadas

1. **OpenAI** — Prompt Engineering: https://platform.openai.com/docs/guides/prompt-engineering
2. **OpenAI** — Prompting overview: https://platform.openai.com/docs/guides/prompting
3. **Anthropic** — Prompt engineering overview: https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/overview
4. **Anthropic** — Prompting best practices: https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/claude-prompting-best-practices
5. **DAIR.AI** — Prompt Engineering Guide: https://www.promptingguide.ai/
6. **Learn Prompting**: https://learnprompting.org/
7. **Wei et al. (2022)** — Chain-of-Thought: https://arxiv.org/abs/2201.11903
8. **Yao et al. (2022)** — ReAct: https://arxiv.org/abs/2210.03629