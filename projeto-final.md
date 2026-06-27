# Projeto Final — Prompt Engineering na Prática

> Avaliação final do curso "Prompt Engineering na Prática".
> Peso na nota final: 50%.
> Carga horária estimada: 8h (2 semanas).

---

## 1. Objetivo

Avaliar a capacidade do aluno de **aplicar, de forma integrada, os frameworks e técnicas estudados** para resolver um problema real, documentar o processo e avaliar criticamente os resultados usando rúbricas.

---

## 2. Escopo

Cada aluno escolherá **um caso real** — de preferência do seu trabalho, estudo ou rotina — que envolva pelo menos uma das seguintes situações:

| Situação | Exemplos |
|---|---|
| Produção de conteúdo profissional | E-mail comercial, proposta, relatório, post LinkedIn, microcopy de UX |
| Análise ou síntese de informação | Resumo executivo, análise de sentimento, extração de dados de documento |
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
- Escolha UMA das rúbricas-exemplo do `rubrica.md` (seção 8.3 — avaliar prompt; seção 8.4 — avaliar saída)
- Aplique a rúbrica a UM dos 3 prompts/saídas (à sua escolha)
- Entregue a rúbrica preenchida com nota + justificativa por critério

### Entregável 4 — Reflexão final (máx. 300 palavras)
- Qual framework funcionou melhor para o seu caso? Por quê?
- Em que situação você usaria cada framework?
- Qual a principal limitação que você percebeu ao aplicar os frameworks?
- Como você usaria rúbricas no seu dia a dia após este curso?

---

## 4. Cronograma sugerido

| Etapa | Semana | Atividade | Horas |
|---|---|---|---|
| 1 | Semana 1, dias 1-2 | Escolher caso + planejar (Entregável 1) | 1h |
| 2 | Semana 1, dias 3-5 | Construir Prompt 1 e Prompt 2 (frameworks práticos) | 3h |
| 3 | Semana 2, dias 6-8 | Construir Prompt 3 (ReAct ou BDI) + coletar saídas | 2h |
| 4 | Semana 2, dias 9-10 | Aplicar rúbrica + reflexão final + revisão | 2h |
| **Total** | | | **8h** |

---

## 5. Rúbrica de correção do projeto final

Esta rúbrica **analítica** (5 critérios × 4 níveis) será usada pelo instrutor para corrigir o projeto. **Ela deve ser compartilhada com o aluno antes da entrega** (Boa prática: seção 12 do `rubrica.md`).

| Critério | Iniciante (1) | Em desenvolvimento (2) | Proficiente (3) | Avançado (4) |
|---|---|---|---|---|
| **A. Adequação do caso** | Caso trivial ou artificial, que não justifica uso de IA | Caso razoável, mas o uso de IA não traz valor claro | Caso real e adequado, uso de IA justificado | Caso real, complexo e que demostra valor real do uso de IA |
| **B. Aplicação dos frameworks** | Não usa os 3 prompts / não usa 2 frameworks diferentes | Usa 3 prompts mas frameworks mal aplicados (componentes faltando) | Usa 3 prompts com 2 frameworks diferentes, aplicados corretamente | Usa 3 prompts + 2 frameworks + aplicação correta + adaptação criativa ao caso |
| **C. Reflexão crítica** | Reflexão genérica ("deu certo", "gostei") | Reflexão superficial, sem identificar pontos fracos | Reflexão identifica o que funcionou e o que falhou, com justificativa | Reflexão crítica profunda + conecta com conceitos do curso (rúbricas, técnicas) |
| **D. Aplicação da rúbrica** | Não aplica rúbrica / aplica sem justificativa | Aplica rúbrica, mas justificativas são vagas | Aplica rúbrica com justificativas específicas por critério | Aplica rúbrica com justificativas + compara níveis + reconhece limites da própria rúbrica |
| **E. Qualidade da escrita** | Texto confuso, desorganizado, muitos erros | Compreensível, mas com trechos ambíguos ou erros ocasionais | Claro, organizado, sem erros | Claro, organizado, conciso, sem erros, bem estruturado em seções |

### Conversão de nota

- Cada critério tem peso igual (20% cada, nota de 1 a 4)
- Nota bruta = (A + B + C + D + E) ÷ 5 → escala de 1 a 4
- Conversão para escala 0-10: **nota final = (nota bruta − 1) × (10 ÷ 3)**
  - Ex.: nota bruta 3 → nota final = (3−1) × (10/3) = 6,67
  - Ex.: nota bruta 4 → nota final = 10
  - Ex.: nota bruta 2 → nota final = 3,33

**Aprovação:** nota final ≥ 7,0 (equivalente a nota bruta média ≥ 3,1).

---

## 6. Apresentação oral (Aula 12)

Cada aluno tem **5 minutos** para apresentar:

| Tempo | Conteúdo |
|---|---|
| 0-1 min | Caso escolhido e por que usou IA |
| 1-3 min | Os 3 prompts (rapidíssimo) + framework de cada um |
| 3-4 min | Principais achados (o que funcionou/falhou) |
| 4-5 min | Autoavaliação pela rúbrica + próximos passos |

**A apresentação NÃO substitui o arquivo entregável** — ela complementa. A nota final do projeto é composta por:

- **Arquivo entregue:** 80% da nota do projeto
- **Apresentação oral:** 20% da nota do projeto

---

## 7. Casos sugeridos (caso o aluno não tenha um próprio)

### Caso sugerido A — E-mail de proposta comercial
Você trabalha numa agência pequena. Escreva um e-mail de proposta para um cliente prospect (pequeno negócio local) usando 2 frameworks práticos + 1 prompt ReAct para pesquisar informação sobre o prospect.

### Caso sugerido B — Resumo executivo de relatório técnico
Você recebeu um relatório técnico de 10 páginas (use um relatório público real, ex.: relatório de sustentabilidade de uma empresa). Faça um resumo executivo usando CARE + outro framework + um prompt BDI que simule um "analista que avalia o resumo".

### Caso sugerido C — Microcopy de UX
Você é UX designer e precisa escrever 5 mensagens de erro para um app (login, validação, erro de conexão, etc.). Use RACE + CARE + um prompt ReAct que busque boas práticas de UX writing em fontes externas.

---

## 8. Entrega e submissão

- **Formato:** arquivo único em PDF ou `.md` (Markdown)
- **Nomenclatura:** `projeto-final_[nome-aluno].pdf` ou `.md`
- **Prazo:** até o final da Aula 12 (data definida pelo instrutor)
- **Plágio/AI:** é **esperado** que o aluno use LLMs para gerar as saídas — o que está sendo avaliado é a **construção dos prompts** e a **avaliação crítica**, não a saída em si. Copiar projeto de colega é falta grave.

---

## 9. Observação de transparência acadêmica

| Item | Status |
|---|---|
| Rúbrica de correção (seção 5) | ⚠️ **Construção didática própria deste curso** — não é uma rúbrica validada empiricamente. Inspirada nos componentes clássicos (Popham 1997; Herman 1992; Goodrich 1996) documentados no `rubrica.md`. |
| Conversão de nota bruta → escala 0-10 | ⚠️ Fórmula de conversão própria deste curso; pode ser ajustada pelo instrutor. |
| Casos sugeridos (seção 7) | ⚠️ Casos didáticos criados para este curso, não extraídos de literatura. |
| ReAct (caso usado pelo aluno) | ✅ Técnica acadêmica peer-reviewed (Yao et al., 2022). |
| BDI (caso usado pelo aluno) | ✅ Modelo acadêmico formal (Bratman 1987; Rao & Georgeff 1995). |
| RACE, TAG, CARE (caso usados) | ⚠️ Heurísticas práticas — não acadêmicas. O aluno deve sinalizar isso no projeto. |

> **Recomendação:** O instrutor deve calibrar a rúbrica de correção com 2-3 projetos-piloto antes de aplicar à turma completa, para garantir consistência entre avaliadores (boa prática: seção 12 do `rubrica.md`).