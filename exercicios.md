# Exercícios Práticos — Prompt Engineering na Prática

> Curso online de prompt engineering.
> Exercícios por aula, com gabarito comentado.
> Recomendação: o aluno deve executar os exercícios em um LLM real (ChatGPT, Claude ou Gemini) e comparar sua saída com o gabarito.

---

## Como usar este arquivo

- Cada exercício tem: **enunciado**, **dica** (quando relevante), **gabarito** e **critério de autoavaliação**.
- Os gabaritos são **exemplos de resposta esperada**, não respostas únicas — o aluno pode variar desde que atenda aos critérios.
- Os exercícios marcados como **"prática guiada"** devem ser feitos junto com o instrutor; os marcados **"prática livre"** são para entrega.

---

# Módulo 1 — Fundamentos

## Aula 1 — O que é prompt engineering

### Exercício 1.1 (prática guiada)

**Enunciado:** Reformule o prompt vago a seguir em um prompt claro e específico.

> Prompt vago: *"fale sobre ia"*

**Gabarito (exemplo aceitável):**

> *"Explique o conceito de Inteligência Artificial para um público leigo, em até 200 palavras. Use uma analogia do cotidiano e evite jargão técnico. Termine com um exemplo de aplicação prática que o leitor já tenha usado (ex.: recomendação da Netflix, correção ortográfica do celular)."*

**Critério de autoavaliação:**
- [ ] Especificou público?
- [ ] Especificou extensão?
- [ ] Deu diretriz de tom/estilo?
- [ ] Pediu elemento concreto (analogia + exemplo)?

---

### Exercício 1.2 (prática livre)

**Enunciado:** Escolha um prompt vago que você já usou em algum momento e o reformule aplicando os 3 princípios: clareza, especificidade e contexto. Entregue antes/depois.

**Gabarito:** Não há gabarito único. Avalie pela presença dos 3 princípios.

**Critério de autoavaliação:**
- [ ] Antes: prompt com ≤ 8 palavras e sem público/formato definidos
- [ ] Depois: prompt com ≥ 3 dos elementos (público, extensão, tom, formato, exemplo)

---

## Aula 2 — Anatomia de um prompt profissional

### Exercício 2.1 (prática guiada)

**Enunciado:** Decomponha o prompt a seguir nas 5 seções padrão (Identidade, Instruções, Exemplos, Contexto, Entrada).

> *"Você é um revisor de texto experiente em português brasileiro. Revise o texto que vou te passar, corrigindo erros gramaticais e sugerindo melhorias de clareza. Não reescreva o texto inteiro — apenas aponte problemas e sugira correções. Exemplo: se o texto diz 'nós vai', aponte erro de concordância e sugira 'nós vamos'. O texto é para um blog corporativo de RH, tom profissional mas acessível. Texto para revisão: 'A equipe nós vai entregar o relatório amanhã, embora os dados ainda não foi confirmado.'"*

**Gabarito:**

| Seção | Conteúdo do prompt |
|---|---|
| Identidade | "Você é um revisor de texto experiente em português brasileiro." |
| Instruções | "Revise o texto... corrigindo erros gramaticais e sugerindo melhorias de clareza. Não reescreva o texto inteiro — apenas aponte problemas e sugira correções." |
| Exemplos | "Exemplo: se o texto diz 'nós vai', aponte erro de concordância e sugira 'nós vamos'." |
| Contexto | "O texto é para um blog corporativo de RH, tom profissional mas acessível." |
| Entrada | "Texto para revisão: 'A equipe nós vai entregar o relatório amanhã, embora os dados ainda não foi confirmado.'" |

**Critério de autoavaliação:**
- [ ] Identificou as 5 seções corretamente?
- [ ] Notou que a ordem do prompt segue a sequência recomendada?

---

### Exercício 2.2 (prática livre)

**Enunciado:** Escreva um prompt completo com as 5 seções para uma tarefa da sua rotina. Marque cada seção com um comentário `<!-- seção -->`.

**Gabarito:** Avaliado pela presença das 5 seções e pela qualidade da separação entre elas.

---

## Aula 3 — Técnicas estabelecidas

### Exercício 3.1 (prática guiada)

**Enunciado:** Aplique **few-shot prompting** para padronizar o formato de saída de um LLM que classifica sentimento.

**Enunciado detalhado:** Forneça 3 exemplos entrada-saída e peça a classificação de uma 4ª entrada. Formato desejado: `sentimento: [positivo|negativo|neutro] — confiança: [0-100]%`

**Gabarito (exemplo de prompt):**

> Classifique o sentimento dos textos a seguir, no formato `sentimento: [...] — confiança: [...]%`.
>
> Exemplos:
> - "Adorei o produto, chegou rápido e funciona perfeitamente." → sentimento: positivo — confiança: 95%
> - "O produto veio com defeito e ninguém respondeu no suporte." → sentimento: negativo — confiança: 90%
> - "O produto é ok, cumpre o que promete mas nada excepcional." → sentimento: neutro — confiança: 80%
>
> Classifique: "Recebi o produto no prazo, mas a qualidade é inferior ao esperado pela fotos."

**Saída esperada:** `sentimento: negativo (ou neutro) — confiança: ~75%`

**Critério de autoavaliação:**
- [ ] Forneceu ≥ 3 exemplos?
- [ ] Manteve formato idêntico nos exemplos?
- [ ] O LLM respondeu no formato pedido?

---

### Exercício 3.2 (prática livre)

**Enunciado:** Aplique **chain-of-thought** a um problema de raciocínio matemático simples e compare o resultado com e sem o CoT.

**Sugestão de problema:** *"Se 5 máquinas fazem 5 peças em 5 minutos, quantas peças 100 máquinas fazem em 100 minutos?"*

**Gabarito (com CoT):**

> Pense passo a passo antes de responder.
> Se 5 máquinas fazem 5 peças em 5 minutos, cada máquina faz 1 peça em 5 minutos.
> 100 máquinas fazem 100 peças em 5 minutos.
> Em 100 minutos (20 vezes mais tempo), fazem 100 × 20 = 2000 peças.

**Resposta correta:** 2000 peças. (Sem CoT, LLMs frequentemente erram respondendo "100".)

---

# Módulo 2 — Frameworks Práticos

## Aula 4 — Framework RACE

### Exercício 4.1 (prática guiada)

**Enunciado:** Construa um prompt RACE completo para a tarefa: *"escrever um e-mail de follow-up após uma entrevista de emprego"*.

**Gabarito (exemplo):**

> **Role:** Você é um coach de carreira sênior, especializado em comunicação profissional pós-entrevista.
>
> **Action:** Escreva um e-mail de follow-up de agradecimento após uma entrevista para uma vaga de Analista de Dados.
>
> **Context:** A entrevista foi há 2 dias com uma empresa fintech. O candidato é júnior, primeira experiência na área. O recrutador se chamava Marina e mencionou que a resposta sairia em até 7 dias úteis. O candidato não tem experiência prévia em fintech, mas tem portfólio em GitHub.
>
> **Expectation:** E-mail em português, máximo 150 palavras, tom profissional mas acolhedor. Deve incluir: agradecimento, menção a um ponto específico da entrevista, reforço de interesse e CTA sutil ("fico à disposição para mais informações"). Não use jargão corporativo.

**Critério de autoavaliação (rúbrica RACE simplificada):**
- [ ] Role específico (domínio + senioridade)?
- [ ] Action com verbo ativo?
- [ ] Context com ≥ 3 detalhes relevantes?
- [ ] Expectation com formato + extensão + tom + ≥ 1 critério mensurável?

---

### Exercício 4.2 (prática livre)

**Enunciado:** Construa um prompt RACE para uma tarefa real do seu trabalho. Entregue: o prompt + a saída que obteve + uma autoavaliação em 1 parágrafo.

---

## Aula 5 — Framework TAG

### Exercício 5.1 (prática guiada)

**Enunciado:** Converta o prompt RACE da Aula 4 (exercício 4.1) em um prompt TAG, mantendo apenas o essencial.

**Gabarito (exemplo):**

> **Task:** Escrever um e-mail de follow-up de agradecimento após entrevista para vaga de Analista de Dados júnior em fintech.
>
> **Action:** Redigir e-mail profissional, mencionando um ponto específico da entrevista (recrutadora Marina, resposta em 7 dias úteis), reforçando interesse e disponibilidade para mais informações.
>
> **Goal:** E-mail enviado à recrutadora, máximo 150 palavras, tom profissional acolhedor, que mantenha o candidato na consideração da empresa.

**Comparação RACE vs TAG (a discutir com a turma):**
- TAG é ~30% menor que RACE.
- TAG perdeu o Role explícito — a IA pode não "assumir" o papel de coach de carreira.
- TAG funciona aqui porque o contexto é evidente; em tarefas técnicas com menos óbvias, RACE seria melhor.

---

### Exercício 5.2 (prática livre)

**Enunciado:** Aplique TAG a uma tarefa de **tradução** (EN → PT-BR) e a uma tarefa de **geração de 10 headlines** para um post de LinkedIn sobre IA. Entregue os dois prompts e as saídas.

---

## Aula 6 — Framework CARE

### Exercício 6.1 (prática guiada)

**Enunciado:** Construa um prompt CARE (versão NN/G) para um e-mail de **proposta comercial** a ser enviado a um cliente potencial.

**Gabarito (exemplo):**

> **Context:**
> Sou sócio de uma pequena agência de marketing digital (5 pessoas) em São Paulo. Atendo pequenos negócios locais. O cliente prospect é uma cafeteria de bairro que tem Instagram mas não usa para atrair clientes — só posta fotos aleatórias. Dona: Carla, 40 anos, sem formação em marketing, responde mensagens em horário comercial.
>
> **Ask:**
> Você é um copywriter comercial experiente. Escreva um e-mail de proposta para a Carla. Siga estes passos:
> 1. Escreva um subject line que desperte curiosidade sem ser clickbait.
> 2. No corpo do e-mail, comece reconhecendo o que ela já faz bem (postar fotos).
> 3. Apresente 2 serviços específicos que cabem no orçamento de pequeno negócio (não mencione pacote corporativo).
> 4. Termine com CTA de baixo atrito (15 min de call, horário comercial).
>
> **Rules:**
> - Tom: conversacional e próximo, não formal.
> - Não use "inovador", "disruptivo", "solução completa".
> - Não mencione preços.
> - Máximo 180 palavras.
> - Use "você", não "a senhora".
>
> **Examples:**
> ✓ Bom subject line: "3 cafeterias que dobraram clientes com Instagram (sem pagar tráfego)"
> ✗ Mau subject line: "Proposta comercial — Soluções Inovadoras para o Seu Negócio"
> ✓ Tom que quero: "Oi Carla, vi as fotos do cappuccino de domingo — ficaram ótimas. Quer bater um papo sobre como fazer isso atrair mais clientes na sua rua?"

**Critério de autoavaliação (rúbrica CARE simplificada):**
- [ ] Context com ≥ 4 detalhes (papel, público, situação, restrições)?
- [ ] Ask com passos numerados?
- [ ] Rules com ≥ 3 restrições (tom + palavras proibidas + extensão)?
- [ ] Examples com bom e mau exemplo?

---

### Exercício 6.2 (prática livre)

**Enunciado:** Construa um prompt CARE para uma tarefa em que você já tenha dificuldade com IA generativa (algo em que ela costuma falhar com você). Entregue: o prompt + a saída + reflexão (1 parágrafo) sobre se o CARE resolveu o problema.

---

# Módulo 3 — Técnicas Avançadas

## Aula 7 — ReAct

### Exercício 7.1 (prática guiada)

**Enunciado:** Escreva a **trajetória Thought/Action/Observation** (sem executar, apenas planejando) para responder a esta pergunta: *"Qual o PIB per capita do país onde nasceu o criador da linguagem Python?"*

**Gabarito (trajetória esperada):**

```
Thought 1: Preciso descobrir quem criou a linguagem Python.
Action 1: Search[criador da linguagem Python]
Observation 1: Guido van Rossum, nascido nos Países Baixos (Holanda).

Thought 2: Preciso descobrir o PIB per capita dos Países Baixos.
Action 2: Search[PIB per capita Países Baixos]
Observation 2: ~US$ 60.000 (valor varia conforme fonte/ano).

Thought 3: Posso dar a resposta.
Action 3: Finish[O criador do Python é Guido van Rossum, nascido nos Países Baixos. O PIB per capita do país é aproximadamente US$ 60.000 (valor varia por ano/fonte).]
```

**Critério de autoavaliação:**
- [ ] Cada Thought justifica o próximo Action?
- [ ] Cada Action chama uma ferramenta de busca?
- [ ] A resposta final integra as duas observações?

---

### Exercício 7.2 (prática livre)

**Enunciado:** Crie uma pergunta que exija 3+ buscas externas encadeadas e escreva a trajetória Thought/Action/Observation esperada. Tema livre (ex.: histórico, ciência, geografia).

---

## Aula 8 — BDI

### Exercício 8.1 (prática guiada)

**Enunciado:** Construa um prompt no formato BDI (analogia) para um **planejador financeiro pessoal** que deve ajudar um usuário a decidir entre pagar dívida ou investir.

**Gabarito (exemplo):**

> **Beliefs:** Você é um consultor financeiro certificado CFP. Assuma que a inflação atual está em ~4,5% ao ano, que dívidas de cartão de crédito têm juros de ~12% ao mês e que investimentos conservadores rendem ~0,8% ao mês + CDI. Considere o perfil do usuário: dívida de R$ 8.000 no cartão, reserva de R$ 3.000 guardada em poupança, renda líquida R$ 4.500/mês, gastos essenciais R$ 3.000/mês.
>
> **Desires:** (1) Recomendar a melhor alocação entre "quitar dívida" e "investir", (2) explicar o racional economicamente, (3) propor um plano de 3 meses.
>
> **Intentions:** (1) Calcular o custo financeiro de manter a dívida por mais 3 meses (juros compostos); (2) calcular o ganho alternativo de investir a reserva; (3) comparar e indicar a decisão; (4) detalhar passo a passo do plano recomendado em tópicos curtos; (5) alertar para o risco de zerar a reserva e voltar a endividar.

**Critério de autoavaliação:**
- [ ] Beliefs contém pelo menos 1 fato sobre o mundo + 1 regra do domínio?
- [ ] Desires são objetivos que o agente deve perseguir?
- [ ] Intentions são planos/passos concretos e executáveis?

---

### Exercício 8.2 (prática livre)

**Enunciado:** Aplique o formato BDI a um caso que exija "agente com estado interno" do seu interesse: assistente jurídico, planejador de viagem, tutor de idiomas, etc. Entregue o prompt + a saída obtida + reflexão sobre se a analogia BDI ajudou (vs um prompt RACE simples para o mesmo caso).

---

# Módulo 4 — Avaliação com Rúbricas

## Aula 9 — O que é rúbrica e como construí-la

### Exercício 9.1 (prática guiada)

**Enunciado:** Construa uma rúbrica analítica simples (3 critérios × 4 níveis) para avaliar um **resumo executivo** (1 página). Preencha os descritores.

**Gabarito (exemplo):**

| Critério | Iniciante (1) | Em desenvolvimento (2) | Proficiente (3) | Avançado (4) |
|---|---|---|---|---|
| **Clareza** | Confuso, exige releitura múltipla | Compreensível, mas com trechos ambíguos | Claro do início ao fim | Claro e conciso, sem redundância |
| **Estrutura** | Sem seções identificáveis | Seções presentes mas desordenadas | Seções padrão (intro, achados, conclusão) | Seções bem definidas + hierarquia visível |
| **Aderência ao objetivo** | Não responde ao objetivo do resumo | Responde parcialmente | Responde ao objetivo | Responde + antecipa perguntas do leitor |

**Critério de autoavaliação:**
- [ ] 3 critérios distintos (sem sobreposição)?
- [ ] 4 níveis com descritores **observáveis** (não inferencia)?
- [ ] Descritores diferenciam claramente os níveis?

---

### Exercício 9.2 (prática livre)

**Enunciado:** Construa uma rúbrica analítica (4 critérios × 4 níveis) para avaliar uma **apresentação de slides** (10 min). Justifique a escolha dos critérios em 1 parágrafo.

---

## Aula 10 — Rúbricas para prompt engineering

### Exercício 10.1 (prática guiada)

**Enunciado:** Use a rúbrica-exemplo de saída de IA (seção 8.4 do `rubrica.md`) para avaliar a resposta abaixo, que foi gerada para o prompt: *"Explique o que é blockchain em 100 palavras para leigo"*.

> **Resposta da IA:** "Blockchain é uma tecnologia legal que funciona como um caderninho digital onde tudo fica registrado. Imagina um livro-razão compartilhado entre várias pessoas, ninguém consegue mexer no que já foi escrito. Cada bloco tem informações e liga com o anterior por um código matemático. É seguro porque todo mundo tem uma cópia, então se alguém tentar trapacear os outros notam. Usam em criptomoedas tipo Bitcoin. Algumas empresas querem usar para contratos também. É complicado mas promissor."

**Gabarito (avaliação esperada):**

| Critério | Nota | Justificativa |
|---|---|---|
| Precisão factual | 2 (Em desenvolvimento) | "livro-razão compartilhado" é razãoável; "código matemático" é vago; não há erros crassos mas faltam precisões |
| Aderência ao prompt | 2 | Cumpriu "leigo" e "100 palavras" (~95 palavras), mas não respeitou a extensão exata; faltou estrutura |
| Clareza | 3 (Proficiente) | Claro, usa analogia acessível ("caderninho", "livro-razão") |
| Formatação | 1 (Iniciante) | Sem estrutura, parágrafo único, sem destaques |
| Tom/Registro | 3 | Adequado a leigo, conversacional sem ser informal demais |

**Nota final (média):** 2,2 / 4 → 5,5 / 10

**Critério de autoavaliação:**
- [ ] Justificou cada nota com trecho da resposta?
- [ ] Notas são consistentes com os descritores da rúbrica?
- [ ] Conseguiu diferenciar níveis (não deu tudo 3 ou tudo 2)?

---

### Exercício 10.2 (prática livre)

**Enunciado:** Peça a um LLM um resumo de um tema que você domina (para poder avaliar a qualidade) usando um prompt simples. Aplique a rúbrica de saída de IA (seção 8.4 do `rubrica.md`) e entregue: prompt + resposta + rúbrica preenchida + nota final.

---

# Módulo 5 — Projeto Final

## Aula 11 — Orientação

### Exercício 11.1 (entrega obrigatória)

**Enunciado:** Escolha o caso para seu projeto final. Entregue:
1. Descrição do caso (1 parágrafo)
2. Frameworks que pretende aplicar (2 no mínimo, justificando a escolha)
3. Rúbrica que pretende usar (cite a seção do `rubrica.md`)
4. Cronograma (datas para cada etapa)

**Gabarito:** Não há. Avaliação é formativa — feedback do instrutor para refinar o escopo.

---

## Aula 12 — Defesa

### Exercício 12.1 (entrega obrigatória)

**Enunciado:** Entregue o projeto final completo conforme especificado em `projeto-final.md`. Prepare uma apresentação de 5 minutos cobrindo: caso, prompts construídos, frameworks usados, principais achados, autoavaliação pela rúbrica.

---

# Síntese dos exercícios por aula

| Aula | Exercício | Tipo | Entrega |
|---|---|---|---|
| 1 | 1.1 Reformular prompt vago | Guiado | Autoavaliação |
| 1 | 1.2 Reformular prompt próprio | Livre | Fórum |
| 2 | 2.1 Decompor 5 seções | Guiado | Autoavaliação |
| 2 | 2.2 Escrever prompt com 5 seções | Livre | Fórum |
| 3 | 3.1 Few-shot classificação | Guiado | Autoavaliação |
| 3 | 3.2 CoT problema matemático | Livre | Fórum |
| 4 | 4.1 RACE e-mail follow-up | Guiado | Autoavaliação |
| 4 | 4.2 RACE tarefa própria | Livre | Fórum |
| 5 | 5.1 Converter RACE→TAG | Guiado | Autoavaliação |
| 5 | 5.2 TAG tradução + headlines | Livre | Fórum |
| 6 | 6.1 CARE proposta comercial | Guiado | Autoavaliação |
| 6 | 6.2 CARE problema difícil | Livre | Fórum |
| 7 | 7.1 Trajetória ReAct | Guiado | Autoavaliação |
| 7 | 7.2 Pergunta 3+ buscas | Livre | Fórum |
| 8 | 8.1 BDI planejador financeiro | Guiado | Autoavaliação |
| 8 | 8.2 BDI caso próprio | Livre | Fórum |
| 9 | 9.1 Rúbrica resumo executivo | Guiado | Autoavaliação |
| 9 | 9.2 Rúbrica apresentação | Livre | Fórum |
| 10 | 10.1 Avaliar resposta de IA | Guiado | Autoavaliação |
| 10 | 10.2 Avaliar resumo de tema próprio | Livre | Fórum |
| 11 | 11.1 Proposta de projeto | Livre | Instrutor |
| 12 | 12.1 Projeto final + defesa | Livre | Banca |

---

## Observação metodológica

- Os gabaritos são **exemplos de resposta aceitável**, não respostas únicas. Variações são bem-vindas desde que atendam aos critérios.
- Exercícios "guiados" são demonstrados pelo instrutor em aula e o aluno os reproduz.
- Exercícios "livres" exigem que o aluno traga um caso próprio — isso garante relevância prática.
- A rúbrica de prompt RACE (seção 8.3 do `rubrica.md`) pode ser usada para corrigir os exercícios 4.1, 4.2, 5.1, 6.1 e 6.2.
- A rúbrica de saída de IA (seção 8.4 do `rubrica.md`) pode ser usada para avaliar as saídas geradas em qualquer exercício.