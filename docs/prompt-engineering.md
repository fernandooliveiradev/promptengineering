# Prompt Engineering

> Documentação de apoio para cursos online.
> Fontes verificadas: documentação oficial da OpenAI e da Anthropic, Prompt Engineering Guide (DAIR.AI) e Learn Prompting — links ao final.

---

## 1. Definição

**Prompt Engineering** (Engenharia de Prompts) é a disciplina que estuda como **estruturar instruções (prompts)** para modelos de linguagem (LLMs) de modo a obter respostas **consistentes, precisas e úteis**.

Trata-se de uma combinação entre **arte e ciência**: o modelo é probabilístico (não determinístico), portanto o prompt precisa guiar a geração de tokens sem garantir uma saída única.

Em termos formais, dado um modelo \( M \) e um prompt \( p \), buscamos:

\[
M(p) \rightarrow y \quad \text{tal que} \quad y \approx y^*
\]

onde \( y^* \) é a resposta ideal desejada. O papel do engenheiro de prompts é projetar \( p \) para maximizar a probabilidade de \( y \approx y^* \).

---

## 2. Princípios fundamentais

### 2.1 Clareza e especificidade
Modelos respondem melhor a instruções **explícitas**. A regra prática: *mostre seu prompt a um colega sem contexto; se ele ficar confuso, o modelo também ficará*.

### 2.2 Estruturação lógica
Separar o prompt em seções distintas (identidade, instruções, exemplos, contexto) reduz ambiguidade. Formatos como **Markdown** e **tags XML** são amplamente recomendados para delimitar blocos.

### 2.3 Exemplos (*few-shot prompting*)
Fornecer 3–5 exemplos representativos melhora a aderência ao formato, tom e estrutura esperados.

### 2.4 Cadeia de pensamento (*chain-of-thought*)
Pedir ao modelo que raciocine passo a passo antes de dar a resposta final tende a melhorar resultados em tarefas que exigem raciocínio multi-etapas.

### 2.5 Definição de papel (*role prompting*)
Atribuir uma persona/rol ("Você é um auditor fiscal sênior...") foca o comportamento e o tom do modelo.

---

## 3. Anatomia de um prompt bem estruturado

Um prompt profissional geralmente contém, em ordem:

| Seção | Função |
|------|--------|
| **Identidade** | Define quem é o assistente (persona, estilo, objetivo). |
| **Instruções** | Regas de comportamento, o que fazer e o que NÃO fazer. |
| **Exemplos** | Casos de entrada/saída esperados (*few-shot*). |
| **Contexto** | Dados de apoio, documentos, variáveis dinâmicas. |
| **Entrada** | A tarefa/consulta específica do usuário. |

---

## 4. Técnicas estabelecidas

| Técnica | Quando usar |
|---------|-------------|
| **Zero-shot** | Quando o modelo já compreende bem a tarefa pela instrução. |
| **Few-shot / Multishot** | Para padronizar formato e estilo. |
| **Chain-of-thought (CoT)** | Tarefas de raciocínio, matemática, lógica. |
| **Role prompting** | Focar domínio e tom. |
| **Structured output (JSON)** | Quando a saída será consumida por código. |
| **Prompt chaining** | Dividir tarefas complexas em chamadas sequenciais. |

---

## 5. Boas práticas de produção

- **Versionar prompts no código-fonte**, não em interfaces externas não auditáveis.
- Criar **suites de avaliação** (*evals*) que meçam o comportamento do prompt frente a casos de teste.
- Fixar **snapshots de modelo** em produção para evitar flutuações de comportamento entre versões.
- Especificar o **formato de saída** desejado de forma positiva ("responda em parágrafos corridos") em vez de negativa ("não use markdown").
- Pedir ao modelo que **cite trechos** do contexto antes de responder, em tarefas com documentos longos.

---

## 6. Referências (verificadas)

### Documentação oficial de fabricantes
1. **OpenAI** — Prompt Engineering: https://platform.openai.com/docs/guides/prompt-engineering
2. **OpenAI** — Prompting overview: https://platform.openai.com/docs/guides/prompting
3. **Anthropic** — Prompt engineering overview: https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/overview
4. **Anthropic** — Prompting best practices: https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/claude-prompting-best-practices

### Guias de referência da comunidade (autoritativos)
5. **Prompt Engineering Guide (DAIR.AI)**: https://www.promptingguide.ai/
   - Introdução: https://www.promptingguide.ai/introduction
   - Técnicas: https://www.promptingguide.ai/techniques
   - Elementos do prompt: https://www.promptingguide.ai/introduction/elements
6. **Learn Prompting**: https://learnprompting.org/
   - Documentação: https://learnprompting.org/docs/introduction

### Papers seminais das técnicas citadas
7. **Wei et al. (2022)** — *Chain-of-Thought Prompting Elicits Reasoning in Large Language Models*. arXiv:2201.11903. https://arxiv.org/abs/2201.11903
8. **Yao et al. (2022)** — *ReAct: Synergizing Reasoning and Acting in Language Models*. arXiv:2210.03629. https://arxiv.org/abs/2210.03629

---

## 7. Observação metodológica

As técnicas descritas neste documento são **conceitos consolidados** na literatura de prompt engineering, verificadas nas seguintes fontes autoritativas: documentação oficial da **OpenAI** e da **Anthropic**, o **Prompt Engineering Guide** (DAIR.AI, promptingguide.ai) e o **Learn Prompting** (learnprompting.org). Todas as URLs listadas na seção 6 foram verificadas como ativas em jun/2026.

Os detalhes específicos de cada modelo (parâmetros como `temperature`, `top_p`, *reasoning effort*, *extended thinking*) variam conforme o provedor e a versão do modelo. Consulte sempre a documentação vigente do fabricante antes de colocar prompts em produção.