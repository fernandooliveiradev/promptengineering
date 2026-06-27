# Unidade 7 — Rúbricas: conceito e aplicação em prompt engineering

> Curso: Prompt Engineering na Prática
> Materiais: vídeo (12-15 min) + apresentação + infográfico
> Carga horária: 3h (vídeo + leitura + 3 exercícios)

---

## 1. Objetivos de aprendizagem

Ao final desta unidade, o aluno será capaz de:

1. **Definir** rúbrica, seus componentes e tipos (holística, analítica, de desenvolvimento).
2. **Construir** uma rúbrica analítica simples (3-4 critérios × 4 níveis).
3. **Aplicar** rúbricas para avaliar prompts (seguindo RACE/TAG/CARE) e saídas de IA.
4. **Reconhecer** o status acadêmico das rúbricas (consolidadas) vs as rúbricas específicas para prompt engineering (construção didática).

---

## 2. Conteúdo

### Aula 7.1 — O que é rúbrica e como construí-la

#### 2.1 Definição

Uma **rúbrica** (do inglês *rubric*) é um **instrumento de avaliação** que descreve, de forma explícita, as expectativas de desempenho do instrutor para uma tarefa ou trabalho.

> *"A rubric is a scoring guide used to evaluate the quality of students' constructed responses."* — James Popham (1997)

Tipicamente apresentada em formato tabular, uma rúbrica contém:
- **critérios** (*criteria*): os aspectos de desempenho que serão avaliados;
- **descritores** (*descriptors*): as características associadas a cada nível de cada critério;
- **níveis de desempenho** (*performance levels*): uma escala que identifica o grau de domínio em cada critério.

Ela cumpre **papel duplo**:
1. **Para o professor/orientador:** guia a correção, tornando-a mais consistente e rápida.
2. **Para o aluno:** explicita expectativas e padrões, permitindo autoavaliação.

#### 2.2 Componentes

Segundo Herman, Aschbacher e Winters (1992):

| Componente | Descrição |
|---|---|
| **Traços/dimensões** | Os critérios que servem de base para julgar a resposta |
| **Definições e exemplos** | Esclarecem cada traço/dimensão |
| **Escala de valores** | Graduação para classificar cada dimensão (ex.: Iniciante, Em desenvolvimento, Proficiente, Avançado) |
| **Padrões de excelência** | Modelos ou exemplos que ilustram níveis específicos |

#### 2.3 Tipos

| Tipo | Característica | Quando usar |
|---|---|---|
| **Holística** | Uma nota global para o trabalho inteiro | Avaliações rápidas, feedback sumário |
| **Analítica** | Avalia cada dimensão separadamente | Feedback detalhado, identificar pontos fortes/fracos |
| **De Desenvolvimento** | Subtipo da analítica; mapeia modos de prática numa comunidade | Apoiar aprendizagem transformacional |

#### 2.4 Benefícios comprovados

**Para instrutores:**
- Reduz tempo de correção
- Identifica tendências da turma
- Garante consistência entre avaliadores
- Reduz incerteza
- Inibe contestações de notas

**Para estudantes:**
- Compreende expectativas e padrões
- Usa feedback para melhorar
- Autoavalia e monitora progresso
- Reconhece pontos fortes e fracos

#### 2.5 Como criar — método de 5 passos (Goodrich, 1996)

| Passo | Ação |
|---|---|
| **1** | **Model Review:** Apresente exemplos de trabalhos de qualidade variada |
| **2** | **Criteria Listing:** Liste colaborativamente os critérios, incorporando feedback dos alunos |
| **3** | **Quality Gradations:** Defina categorias hierárquicas de qualidade |
| **4** | **Practice on Models:** Permita que os alunos apliquem a rúbrica a trabalhos-exemplo |
| **5** | **Self and Peer Assessment:** Introduza auto e heteroavaliação |

#### 2.6 Roteiro operacional para o instrutor

```
1. Defina os objetivos de aprendizagem da tarefa.
2. Liste 3-7 critérios (dimensões) que importam para o sucesso da tarefa.
3. Para cada critério, escreva descritores claros para cada nível da escala.
4. Defina a escala (ex.: 4 níveis — Iniciante, Em desenvolvimento, Proficiente, Avançado).
5. Atribua pesos se algumas dimensões forem mais importantes que outras.
6. Teste a rúbrica em trabalhos-exemplo e refine os descritores ambíguos.
7. Compartilhe a rúbrica com os alunos ANTES da entrega do trabalho.
```

#### 2.7 Anatomia visual de uma rúbrica analítica

```
                   | Nível 1        | Nível 2        | Nível 3        | Nível 4
                   | (Iniciante)    | (Em desen-     | (Proficiente)  | (Avançado)
                   |                | volvimento)   |                |
-------------------|----------------|----------------|----------------|-----------
Critério A         | descritor A1   | descritor A2   | descritor A3   | descritor A4
(ex.: Clareza)     |                |                |                |
-------------------|----------------|----------------|----------------|-----------
Critério B         | descritor B1   | descritor B2   | descritor B3   | descritor B4
(ex.: Argumento)   |                |                |                |
```

Descritores devem ser: **observáveis**, **específicos**, **diferenciados** entre níveis, **compartilhados** antes da entrega.

---

### Aula 7.2 — Rúbricas para prompt engineering

#### 2.8 Por que rúbricas importam para prompt engineering

Rúbricas são **a ponte entre os frameworks (RACE, TAG, CARE) e a avaliação objetiva de resultados**. Sem rúbrica, julgar se um prompt é "bom" fica subjetivo. Com rúbrica, transforma-se a avaliação em **processo replicável, auditável e ensinável**.

#### 2.9 Três usos típicos em cursos de IA

| Uso | O que avalia | Exemplo de critério |
|---|---|---|
| **Avaliar prompts dos alunos** | Se o prompt segue um framework | "Presença de Role explícita e específica" (RACE) |
| **Avaliar saídas da IA** | Qualidade da resposta gerada | "Precisão factual: sem alucinações verificáveis" |
| **Avaliar competência geral** | Teoria + prática | "Aplica o framework adequado ao tipo de tarefa" |

#### 2.10 Rúbrica-exemplo: Avaliar um prompt construído com RACE

| Critério | Iniciante (1) | Em desenvolvimento (2) | Proficiente (3) | Avançado (4) |
|---|---|---|---|---|
| **Role (R)** | Ausente ou genérico | Presente, mas vago | Presente e específico | Presente, específico e com especialização relevante |
| **Action (A)** | Ausente ou ambígua | Presente, mas sem verbo forte | Verbo ativo claro + objeto | Verbo + objeto + método explicitados |
| **Context (C)** | Ausente | Parcial | Completo | Completo + dados que ancoram a IA |
| **Expectation (E)** | Ausente | Apenas formato | Formato + extensão + tom | Formato + extensão + tom + critérios mensuráveis |

#### 2.11 Rúbrica-exemplo: Avaliar a saída de uma IA generativa

| Critério | Iniciante (1) | Em desenvolvimento (2) | Proficiente (3) | Avançado (4) |
|---|---|---|---|---|
| **Precisão factual** | Erros verificáveis/alucinações | Maioria correta, alguns erros | Sem erros óbvios | Fatos checáveis e fontes confiáveis |
| **Aderência ao prompt** | Ignora ≥2 instruções | Cumpre a maioria | Cumpre todas | Cumpre + antecipa implicações |
| **Clareza** | Confusa ou desorganizada | Compreensível com releitura | Clara e bem estruturada | Clara, estruturada e envolvente |
| **Formatação** | Não segue formato | Segue parcialmente | Segue formato pedido | Segue + usa formatação apropriada |
| **Tom/Registro** | Inadequado ao público | Adequado em partes | Adequado ao público-alvo | Adequado + consistente |

#### 2.12 Boas práticas resumidas

| Boa prática | Por quê |
|---|---|
| Compartilhe a rúbrica **antes** da entrega | Alinha expectativas |
| Use descritores **observáveis** | Reduz subjetividade |
| Limite a 3-7 critérios | Rúbrica muito longa perde utilidade |
| **Teste a rúbrica** em trabalhos-exemplo | Revela descritores ambíguos |
| Atribua **pesos** se dimensões têm importância diferente | Reflete prioridade real |
| **Calibre** com outros avaliadores | Garante consistência |
| Conecte cada critério a um **objetivo de aprendizagem** | Garante validade |
| Use **auto e heteroavaliação** | Reforça aprendizagem |

---

## 3. Exercícios da unidade

### Exercício 7.1 — Rúbrica para resumo executivo (guiado)
Construa uma rúbrica analítica (3 critérios × 4 níveis) para avaliar um resumo executivo. **Gabarito no `exercicios.md`.**

### Exercício 7.2 — Rúbrica para apresentação (livre)
Construa uma rúbrica analítica (4 critérios × 4 níveis) para avaliar uma apresentação de slides (10 min). Justifique a escolha dos critérios em 1 parágrafo.

### Exercício 7.3 — Avaliar resposta de IA (guiado)
Use a rúbrica-exemplo de saída de IA (seção 2.11) para avaliar uma resposta de LLM sobre "o que é blockchain em 100 palavras para leigo". **Gabarito no `exercicios.md`.**

---

## 4. Leitura complementar

- `docs/rubrica.md` — documento base completo com rúbricas de desenvolvimento, etimologia, aspectos técnicos

---

## 5. Fontes verificadas

1. **Carnegie Mellon University — Eberly Center.** *Creating and Using Rubrics*. https://www.cmu.edu/teaching/assessment/assesslearning/rubrics.html
2. **Wikipedia** — *Rubric (academic)*. https://en.wikipedia.org/wiki/Rubric_(academic)

### Referências acadêmicas primárias
3. **Popham, W. J.** (1997). *What's Wrong - and What's Right - with Rubrics*. Educational Leadership, 55(2), 72–75.
4. **Herman, J. L. et al.** (1992). *A Practical Guide to Alternative Assessment*. ASCD.
5. **Goodrich, H.** (1996). *Understanding Rubrics*. Educational Leadership, 54(4), 14–18.
6. **Dawson, P.** (2015). *Assessment rubrics: towards clearer and more replicable design*. Assessment & Evaluation in Higher Education, 42(3), 347–360.
7. **Dirlam, D. K.** (2017). *Teachers, Learners, Modes of Practice*. Routledge.

> **Transparência acadêmica:**
> - **Conceito de rúbrica** (seções 2.1-2.7): ✅ literatura acadêmica consolidada (Popham, Herman, Goodrich, Dawson, Dirlam).
> - **Rúbricas para prompt engineering** (seções 2.10 e 2.11): ⚠️ **construção didática própria deste curso**, não validadas empiricamente. Inspiradas nos componentes clássicos documentados na literatura.