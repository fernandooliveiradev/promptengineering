# Unidade 8 — Projeto Final

> Curso: Prompt Engineering na Prática
> Materiais: vídeo (15-20 min) + apresentação + infográfico
> Carga horária: 8h (2 semanas)
> Peso na nota final: 50%

---

## 1. Objetivos de aprendizagem

Ao final desta unidade, o aluno será capaz de:

1. **Integrar** os frameworks e técnicas estudados num projeto real.
2. **Construir** 3 prompts usando 2 frameworks diferentes obrigatoriamente.
3. **Aplicar** uma rúbrica para avaliar criticamente prompt e/ou saída.
4. **Documentar** o processo com reflexão crítica estruturada.
5. **Defender** o projeto oralmente em 5 minutos.

---

## 2. Escopo

Cada aluno escolherá **um caso real** — de preferência do seu trabalho, estudo ou rotina — que envolva pelo menos uma das seguintes situações:

| Situação | Exemplos |
|---|---|
| Produção de conteúdo profissional | E-mail comercial, proposta, relatório, post LinkedIn, microcopy de UX |
| Análise ou síntese de informação | Resumo executivo, análise de sentimento, extração de dados |
| Tarefa que exige raciocínio multi-etapas | Planejamento, decisão entre alternativas, diagnóstico |
| Tarefa que exige informação externa | Pergunta que precisa de busca (ReAct) |

> ⚠️ **Caso não tenha um caso próprio**, use um dos 3 casos sugeridos na seção 7.

---

## 3. Entregáveis

O aluno deve entregar **um único arquivo** (PDF ou Markdown) contendo:

### Entregável 1 — Descrição do caso (máx. 200 palavras)
- Contexto: onde a tarefa se insere
- Público-alvo da saída
- Por que é uma tarefa que vale usar IA (e não fazer manualmente)

### Entregável 2 — Três prompts construídos
O aluno deve construir **3 prompts** usando **2 frameworks diferentes** obrigatoriamente:
- **Prompt 1:** usando framework da sua escolha (RACE, TAG ou CARE) — **obrigatório**
- **Prompt 2:** usando **outro** framework diferente do Prompt 1 — **obrigatório**
- **Prompt 3:** usando **ReAct** OU **BDI** (ou outro framework avançado) — **obrigatório**

Para cada prompt, o aluno entrega:
- O prompt completo
- O framework usado
- A saída gerada pelo LLM (colar texto)
- Uma reflexão curta (3-5 linhas): o que funcionou, o que falhou, o que ajustaria

### Entregável 3 — Rúbrica de avaliação aplicada
- Escolha UMA das rúbricas-exemplo (seção 2.10 ou 2.11 da Unidade 7)
- Aplique a rúbrica a UM dos 3 prompts/saídas (à sua escolha)
- Entregue a rúbrica preenchida com nota + justificativa por critério

### Entregável 4 — Reflexão final (máx. 300 palavras)
- Qual framework funcionou melhor para o seu caso? Por quê?
- Em que situação você usaria cada framework?
- Qual a principal limitação que você percebeu ao aplicar os frameworks?
- Como você usaria rúbricas no seu dia a dia após este curso?

---

## 4. Cronograma sugerido (2 semanas)

| Etapa | Semana | Atividade | Horas |
|---|---|---|---|
| 1 | S1, dias 1-2 | Escolher caso + planejar (Entregável 1) | 1h |
| 2 | S1, dias 3-5 | Construir Prompt 1 e Prompt 2 (frameworks práticos) | 3h |
| 3 | S2, dias 6-8 | Construir Prompt 3 (ReAct ou BDI) + coletar saídas | 2h |
| 4 | S2, dias 9-10 | Aplicar rúbrica + reflexão final + revisão | 2h |
| **Total** | | | **8h** |

---

## 5. Rúbrica de correção do projeto final

Esta rúbrica **analítica** (5 critérios × 4 níveis) será usada pelo instrutor. **Deve ser compartilhada com o aluno antes da entrega.**

| Critério | Iniciante (1) | Em desenvolvimento (2) | Proficiente (3) | Avançado (4) |
|---|---|---|---|---|
| **A. Adequação do caso** | Trivial ou artificial | Razoável, mas IA não traz valor claro | Real e adequado, uso justificado | Real, complexo, demostra valor da IA |
| **B. Aplicação dos frameworks** | Não usa 3 prompts / 2 frameworks diferentes | Usa 3 prompts mas frameworks mal aplicados | Usa 3 prompts com 2 frameworks diferentes, aplicados corretamente | 3 prompts + 2 frameworks + aplicação correta + adaptação criativa |
| **C. Reflexão crítica** | Genérica ("deu certo", "gostei") | Superficial, sem identificar pontos fracos | Identifica o que funcionou e o que falhou, com justificativa | Crítica profunda + conecta com conceitos do curso |
| **D. Aplicação da rúbrica** | Não aplica / aplica sem justificativa | Aplica, mas justificativas vagas | Aplica com justificativas específicas por critério | Aplica + compara níveis + reconhece limites da rúbrica |
| **E. Qualidade da escrita** | Confuso, desorganizado, muitos erros | Compreensível, com trechos ambíguos | Claro, organizado, sem erros | Claro, organizado, conciso, bem estruturado em seções |

### Conversão de nota

- Cada critério tem peso igual (20%, nota 1-4)
- Nota bruta = (A + B + C + D + E) ÷ 5 → escala 1-4
- Conversão para 0-10: **nota final = (nota bruta − 1) × (10 ÷ 3)**
  - Nota bruta 3 → final 6,67
  - Nota bruta 4 → final 10
  - Nota bruta 2 → final 3,33

**Aprovação:** nota final ≥ 7,0 (nota bruta média ≥ 3,1).

---

## 6. Apresentação oral (5 min por aluno)

| Tempo | Conteúdo |
|---|---|
| 0-1 min | Caso escolhido e por que usou IA |
| 1-3 min | Os 3 prompts (rapidíssimo) + framework de cada um |
| 3-4 min | Principais achados (o que funcionou/falhou) |
| 4-5 min | Autoavaliação pela rúbrica + próximos passos |

**Composição da nota do projeto:**
- Arquivo entregue: 80%
- Apresentação oral: 20%

---

## 7. Casos sugeridos (caso o aluno não tenha um próprio)

### Caso A — E-mail de proposta comercial
Você trabalha numa agência pequena. Escreva um e-mail de proposta para um cliente prospect (pequeno negócio local) usando 2 frameworks práticos + 1 prompt ReAct para pesquisar informação sobre o prospect.

### Caso B — Resumo executivo de relatório técnico
Você recebeu um relatório técnico de 10 páginas (use um relatório público real). Faça um resumo executivo usando CARE + outro framework + um prompt BDI que simule um "analista que avalia o resumo".

### Caso C — Microcopy de UX
Você é UX designer e precisa escrever 5 mensagens de erro para um app (login, validação, erro de conexão, etc.). Use RACE + CARE + um prompt ReAct que busque boas práticas de UX writing em fontes externas.

---

## 8. Entrega e submissão

- **Formato:** arquivo único PDF ou `.md`
- **Nomenclatura:** `projeto-final_[nome-aluno].pdf` ou `.md`
- **Prazo:** até o final da Aula 12
- **Plágio/AI:** é **esperado** que o aluno use LLMs para gerar as saídas — o que está sendo avaliado é a **construção dos prompts** e a **avaliação crítica**, não a saída em si. Copiar projeto de colega é falta grave.

---

## 9. Encerramento do curso

Após o projeto final, o aluno está apto a:

| Competência | Quando usar |
|---|---|
| **TAG** | Tarefas simples e diretas |
| **RACE** | Tarefas com formato controlado |
| **CARE** | Tarefas com contexto rico e exemplo |
| **ReAct** | Tarefas com informação externa |
| **BDI** | Tarefas com agente e estado interno |
| **Rúbricas** | Para avaliar prompts e saídas |

**Aprendizagem contínua:** acompanhe as documentações oficiais (OpenAI, Anthropic, DAIR.AI, Learn Prompting) — prompt engineering muda rápido.

---

## 10. Fontes verificadas (recapitulando o curso)

### Documentação oficial de fabricantes
1. **OpenAI** — https://platform.openai.com/docs/guides/prompt-engineering
2. **Anthropic** — https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/overview

### Guias de referência
3. **DAIR.AI** — https://www.promptingguide.ai/
4. **Learn Prompting** — https://learnprompting.org/

### Frameworks práticos
5. **Prompt Edit** — https://www.promptedit.app/prompt-framework/race
6. **Prompt Edit** — https://www.promptedit.app/prompt-framework/tag
7. **PromptVibe** — https://www.promptvibe.co/frameworks/tag-prompt-framework
8. **Nielsen Norman Group (Kate Moran, 2024)** — https://www.nngroup.com/articles/careful-prompts/

### Técnicas acadêmicas
9. **Yao et al. (2022) — ReAct** — https://arxiv.org/abs/2210.03629
10. **Wei et al. (2022) — CoT** — https://arxiv.org/abs/2201.11903
11. **Rao & Georgeff (1995) — BDI** — https://www.aaai.org/Papers/ICMAS/1995/ICMAS95-042.pdf
12. **Wikipedia — BDI** — https://en.wikipedia.org/wiki/Belief%E2%80%93desire%E2%80%93intention_software_model
13. **Emergent Mind — BDI** — https://www.emergentmind.com/topics/belief-desire-intention-bdi-architecture

### Rúbricas
14. **Carnegie Mellon — Eberly Center** — https://www.cmu.edu/teaching/assessment/assesslearning/rubrics.html
15. **Wikipedia — Rubric** — https://en.wikipedia.org/wiki/Rubric_(academic)
16. **Popham (1997)** — https://eric.ed.gov/?id=EJ552014

---

## 11. Observação de transparência acadêmica

| Componente | Status |
|---|---|
| Prompt engineering (geral) | ✅ Documentação oficial |
| ReAct | ✅ Paper peer-reviewed (Yao 2022) |
| BDI | ✅ Modelo acadêmico formal (Bratman 1987; Rao & Georgeff 1995) |
| RACE, TAG | ⚠️ Heurísticas práticas — não acadêmicas |
| CARE | ⚠️ Heurística prática proposta pela NN/G (não peer-reviewed) |
| Rúbricas (conceito) | ✅ Literatura acadêmica consolidada |
| Rúbricas para prompt engineering (seção 2.10/2.11 Unidade 7) | ⚠️ Construção didática própria |
| Rúbrica de correção do projeto final (seção 5) | ⚠️ Construção didática própria |

> O curso deixa claro quais conteúdos são **técnicas consolidadas** e quais são **heurísticas práticas**. Isso protege a credibilidade do curso e respeita o princípio de não inventar.