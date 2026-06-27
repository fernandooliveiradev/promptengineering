# Roteiros de Gravação — Videoaulas

> Curso "Prompt Engineering na Prática".
> Um roteiro por aula, estruturado em blocos: **Abertura**, **Slides sugeridos**, **Roteiro do instrutor** (fala), **Demo** (quando aplicável), **Fechamento**.
> Duração-alvo: 8-12 min por aula (M1-M4), 15-20 min (M5).

---

## Convenções do roteiro

- `[SLIDE n]` — indica troca de slide
- `[MOSTRAR ...]` — ação visual do instrutor (demo, screenshot, quadro)
- `[FALA]` — texto a ser dito pelo instrutor (pode adaptar)
- `[PAUSA]` — pausa para deixar o aluno absorver
- `[EXERCÍCIO]` — momento de pausar a vídeoaula e fazer exercício
- `[REFERÊNCIA]` — arquivo de leitura complementar

---

# Módulo 1 — Fundamentos

## Aula 1 — O que é prompt engineering e por que importa

### Bloco 1 — Abertura (1 min)

`[SLIDE 1 — título do curso + aula 1]`

`[FALA]` Bem-vindo ao curso Prompt Engineering na Prática. Eu sou [nome] e nesta primeira aula vamos responder uma pergunta simples: o que é prompt engineering e por que você deveria se importar?

`[SLIDE 2 — "fale sobre ia"]`

`[FALA]` Você já digitou algo assim num ChatGPT? "Fale sobre IA". E o que veio? Provavelmente um textão genérico de 500 palavras que não serve para nada. O que faltou? **Engenharia de prompt.**

### Bloco 2 — Definição (3 min)

`[SLIDE 3 — fórmula M(p) → y ≈ y*]`

`[FALA]` Em termos simples: dado um modelo de linguagem M e um prompt p, o modelo gera uma saída y. Nosso objetivo é que y seja o mais próximo possível da resposta ideal y*. O prompt engineering é o processo de projetar p para maximizar essa chance.

`[PAUSA]`

`[FALA]` Importante: o modelo é **probabilístico**, não determinístico. Não há prompt perfeito. Há prompts melhores e prompts piores. É uma mistura de arte e ciência.

`[SLIDE 4 — antes/depois]`

`[FALA]` Veja a diferença. Antes: "fale sobre ia". Depois: "Explique IA para um leigo em 200 palavras, use uma analogia do cotidiano, termine com um exemplo prático que o leitor já tenha usado". A diferença na qualidade da resposta é dramática.

### Bloco 3 — Por que importa (2 min)

`[SLIDE 5 — 3 razões]`

`[FALA]` Três razões para aprender isso agora. Primeiro: IA generativa já é ferramenta de trabalho — você provavelmente já usa. Segundo: a diferença entre um usuário comum e alguém que sabe prompt engineering é de 10x em produtividade. Terceiro: é uma habilidade transferível — funciona com GPT, Claude, Gemini, qualquer LLM.

### Bloco 4 — Exercício guiado (2 min)

`[SLIDE 6 — exercício 1.1]`

`[FALA]` Pause a aula. Pegue um prompt vago que você já usou em algum momento e o reformule aplicando 3 princípios: clareza, especificidade, contexto. Você tem 5 minutos. O gabarito está no arquivo `exercicios.md`, exercício 1.1.

`[EXERCÍCIO]`

### Bloco 5 — Fechamento (1 min)

`[SLIDE 7 — o que vem na próxima aula]`

`[FALA]` Na próxima aula, vamos ver a anatomia completa de um prompt profissional — as 5 seções que todo bom prompt tem. Leitura complementar: arquivo `prompt-engineering.md` seções 1 e 2.

---

## Aula 2 — Anatomia de um prompt profissional

### Bloco 1 — Abertura (1 min)

`[SLIDE 1 — recap aula 1]`

`[FALA]` Na aula passada vimos que prompt engineering é projetar p para que a saída y se aproxime de y*. Hoje vamos dissecar um bom prompt em 5 partes.

### Bloco 2 — As 5 seções (4 min)

`[SLIDE 2 — diagrama das 5 seções: Identidade, Instruções, Exemplos, Contexto, Entrada]`

`[FALA]` Um prompt profissional tipicamente tem 5 seções, nessa ordem: Identidade, Instruções, Exemplos, Contexto, Entrada.

`[SLIDE 3 — seção Identidade]`

`[FALA]` Identidade: quem a IA deve ser. Exemplo: "Você é um revisor de texto experiente em português brasileiro." Quanto mais específico o domínio e senioridade, melhor.

`[SLIDE 4 — seção Instruções]`

`[FALA]` Instruções: o que fazer e o que NÃO fazer. Use verbos ativos. "Revise o texto, corrija erros gramaticais. Não reescreva o texto inteiro."

`[SLIDE 5 — seção Exemplos]`

`[FALA]` Exemplos: 3 a 5 entradas/saídas mostram o padrão. Isso é o que chamamos de few-shot prompting, que veremos na próxima aula.

`[SLIDE 6 — seção Contexto]`

`[FALA]` Contexto: dados de fundo — público, situação, restrições. "O texto é para um blog corporativo de RH, tom profissional."

`[SLIDE 7 — seção Entrada]`

`[FALA]` Entrada: a tarefa específica deste turno. "Texto para revisão: 'A equipe nós vai entregar...'"

### Bloco 3 — Regra de ouro (2 min)

`[SLIDE 8 — regra de ouro]`

`[FALA]` Regra de ouro: mostre seu prompt a um colega sem contexto. Se ele confundir, o modelo também confundirá. Seu colega é o teste mais barato que você tem.

`[PAUSA]`

`[FALA]` Outra dica prática: use **Markdown** (cabeçalhos, listas) e **tags XML** para delimitar blocos. Isso ajuda o modelo a separar Identidade de Contexto de Entrada.

### Bloco 4 — Demo (2 min)

`[MOSTRAR tela com prompt decomposto, destacando cada seção com cor diferente]`

`[FALA]` Veja neste exemplo — destaquei cada seção com uma cor. Repare como a ordem ajuda o modelo a processar na sequência certa.

### Bloco 5 — Exercício (2 min)

`[SLIDE 9 — exercício 2.1]`

`[FALA]` Pause e faça o exercício 2.1 do `exercicios.md`: decomponha um prompt-exemplo nas 5 seções. Marque cada seção. Gabarito no arquivo.

### Bloco 6 — Fechamento (1 min)

`[SLIDE 10 — próxima aula]`

`[FALA]` Na próxima aula veremos 6 técnicas estabelecidas: zero-shot, few-shot, chain-of-thought, role prompting, structured output e prompt chaining.

---

## Aula 3 — Técnicas estabelecidas

### Bloco 1 — Abertura (1 min)

`[SLIDE 1 — recap]`

`[FALA]` Já vimos o que é prompt engineering e a anatomia de um prompt. Hoje: 6 técnicas estabelecidas que você pode aplicar hoje.

### Bloco 2 — As 6 técnicas (6 min)

`[SLIDE 2 — tabela das 6 técnicas]`

`[FALA]` Vou rápido nas 6. Para cada uma: o que é, quando usar.

`[SLIDE 3 — Zero-shot]`

`[FALA]` Zero-shot: quando o modelo já entende a tarefa pela instrução. Ex.: "Resuma este texto em 3 bullets." Não precisa de exemplo. Bom para tarefas comuns.

`[SLIDE 4 — Few-shot]`

`[FALA]` Few-shot: 3-5 exemplos entrada-saída. Útil para padronizar formato, tom, estilo. Vimos isso na seção Exemplos da aula passada.

`[SLIDE 5 — Chain-of-thought]`

`[FALA]` Chain-of-thought: pedir para o modelo pensar passo a passo. Crucial para matemática, lógica, raciocínio. Vamos ver um exemplo na demo.

`[SLIDE 6 — Role prompting]`

`[FALA]` Role prompting: dar uma persona. "Você é um auditor fiscal sênior." Foca o comportamento. É o que chamamos de componente R no framework RACE que veremos no Módulo 2.

`[SLIDE 7 — Structured output]`

`[FALA]` Structured output: pedir JSON. Quando a saída vai para código. Ex.: "Retorne em JSON com campos {sentimento, confiança}."

`[SLIDE 8 — Prompt chaining]`

`[FALA]` Prompt chaining: dividir tarefa complexa em chamadas sequenciais. Ex.: prompt 1 gera esboço, prompt 2 expande cada seção.

### Bloco 3 — Demo CoT (2 min)

`[MOSTRAR tela com ChatGPT aberto, digitando o problema "5 máquinas, 5 peças, 5 minutos..."]`

`[FALA]` Veja este problema clássico. Sem CoT, o modelo frequentemente erra. Com CoT — "pense passo a passo" — ele acerta. Compare as duas saídas lado a lado.

### Bloco 4 — Boas práticas de produção (1 min)

`[SLIDE 9 — boas práticas]`

`[FALA]` Em produção: versionar prompts no código, criar suites de eval, fixar snapshots de modelo, especificar formato de forma positiva (não negativa).

### Bloco 5 — Exercício (1 min)

`[SLIDE 10 — exercícios 3.1 e 3.2]`

`[FALA]` Faça os exercícios 3.1 (few-shot) e 3.2 (CoT com problema matemático). Gabaritos no `exercicios.md`.

### Bloco 6 — Fechamento (1 min)

`[SLIDE 11 — ponte para Módulo 2]`

`[FALA]` Vimos técnicas isoladas. No Módulo 2, vamos organizar tudo em frameworks completos: RACE, TAG, CARE. Até já.

---

# Módulo 2 — Frameworks Práticos

## Aula 4 — Framework RACE

### Bloco 1 — Abertura (1 min)

`[SLIDE 1 — "framework" como organização]`

`[FALA]` Vimos técnicas isoladas. Framework organiza técnicas em estrutura memorável. Hoje: RACE.

### Bloco 2 — Definição (3 min)

`[SLIDE 2 — R·A·C·E]`

`[FALA]` RACE: Role, Action, Context, Expectation. Quatro componentes memoráveis que cobrem as variáveis mais impactantes de um prompt.

`[SLIDE 3 — R: Role]`

`[FALA]` R — Role: a persona. Não diga "você é um designer". Diga "você é um UX designer sênior com 10 anos em mobile". Especificidade importa.

`[SLIDE 4 — A: Action]`

`[FALA]` A — Action: o que fazer, com verbo ativo. "Escreva", "resuma", "compare". Evite "me ajude com".

`[SLIDE 5 — C: Context]`

`[FALA]` C — Context: o componente mais pulado e o maior responsável por saídas genéricas. Inclua público, restrições, situação.

`[SLIDE 6 — E: Expectation]`

`[FALA]` E — Expectation: o formato, extensão, tom. É o que mais controla a qualidade da saída.

### Bloco 3 — Demo (3 min)

`[MOSTRAR prompt RACE completo na tela, com cada componente destacado]`

`[FALA]` Veja este exemplo de prompt RACE para um e-mail de follow-up. Repare: Role específico, Action com verbo ativo, Context com 4 detalhes, Expectation com formato + extensão + tom + critério mensurável.

### Bloco 4 — Quando usar (1 min)

`[SLIDE 7 — quando usar RACE]`

`[FALA]` RACE é bom para escrita profissional, e-mails, resumos, code review. É versátil. Não é bom para tarefas muito simples — aí usamos TAG, que veremos na próxima aula.

### Bloco 5 — Exercício (1 min)

`[SLIDE 8 — exercício 4.1]`

`[FALA]` Faça o exercício 4.1: construa um prompt RACE para um e-mail de follow-up. Gabarito no `exercicios.md`.

### Bloco 6 — Fechamento (1 min)

`[SLIDE 9 — transparência]`

`[FALA]` Importante: RACE é uma **heurística prática**, não uma técnica cientificamente validada. Mas é compatível com todas as técnicas que vimos. Leitura: `race.md`.

---

## Aula 5 — Framework TAG

### Bloco 1 — Abertura (1 min)

`[SLIDE 1 — "menos é mais?"]`

`[FALA]` Nem sempre mais é mais. Para tarefas simples, RACE pode ser over-engineering. Conheça o TAG: o prompt mínimo viável.

### Bloco 2 — Definição (3 min)

`[SLIDE 2 — T·A·G]`

`[FALA]` TAG: Task, Action, Goal. Três componentes que respondem: o que fazer, como fazer, o que é o sucesso.

`[SLIDE 3 — Task vs Action]`

`[FALA]` Diferença crítica que confunde iniciantes: Task é o **escopo** ("escreva um subject line"), Action é o **método** ("gere 5 opções que criem urgência, máximo 50 caracteres"). Task é alto nível, Action é operacional.

`[SLIDE 4 — Goal]`

`[FALA]` Goal é o critério de sucesso. "Aumentar open rate entre assinantes inativos". Sem Goal, a IA otimiza para o alvo errado.

### Bloco 3 — Demo comparativa (3 min)

`[MOSTRAR prompt RACE da aula anterior vs prompt TAG para o mesmo caso]`

`[FALA]` Veja o mesmo caso — e-mail de follow-up — em RACE e em TAG. TAG é 30% menor. Perdeu o Role explícito, mas o contexto era evidente. Funciona aqui.

### Bloco 4 — Quando usar (1 min)

`[SLIDE 5 — quando usar TAG]`

`[FALA]` TAG é bom para: draft rápido, tradução, copy de marketing, listas, reformatação. Não é bom para: tarefas multi-etapas, tarefas que exigem persona especialista.

### Bloco 5 — Exercício (1 min)

`[SLIDE 6 — exercício 5.1]`

`[FALA]` Exercício 5.1: converta o prompt RACE da aula anterior em TAG e compare as saídas. Qual foi melhor para este caso? Por quê?

### Bloco 6 — Fechamento (1 min)

`[SLIDE 7 — ponte para CARE]`

`[FALA]` Para tarefas que precisam de mais contexto — comunicações profissionais, e-mails, propostas — temos o CARE. Próxima aula.

---

## Aula 6 — Framework CARE

### Bloco 1 — Abertura (2 min)

`[SLIDE 1 — cuidado: há duas versões de CARE]`

`[FALA]` Aviso importante: existe **mais de uma definição de CARE** no mercado. Neste curso adotamos a versão da Nielsen Norman Group — a fonte de maior autoridade. Vou explicar por quê.

`[SLIDE 2 — NN/G: Nielsen + Norman]`

`[FALA]` Nielsen Norman Group foi fundada por Jakob Nielsen e Don Norman — o "pai" da disciplina de UX. É a referência mundial em pesquisa de usabilidade. Quando falamos de CARE em UX/escrita profissional, vamos com a NN/G.

### Bloco 2 — Definição (3 min)

`[SLIDE 3 — C·A·R·E (NN/G)]`

`[FALA]` CARE segundo a NN/G: Context, Ask, Rules, Examples. Diferente do RACE, aqui não temos Role — temos Context rico. E onde RACE tem Expectation, CARE tem Rules + Examples.

`[SLIDE 4 — C: Context]`

`[FALA]` Context: a situação. Papel, público, projeto, perfil de usuário. É a moldura do prompt.

`[SLIDE 5 — A: Ask]`

`[FALA]` Ask: a requisição. Pode incluir passos numerados (chain-of-thought) e formato de saída.

`[SLIDE 6 — R: Rules]`

`[FALA]` Rules: as restrições. Tom, extensão, palavras proibidas, guia de estilo. É o que diferencia um prompt profissional de um amador.

`[SLIDE 7 — E: Examples]`

`[FALA]` Examples: bons e maus exemplos. Mostrar > descrever. Um parágrafo de exemplo concreto vale mais que 100 palavras de descrição abstrata.

### Bloco 3 — Demo (3 min)

`[MOSTRAR prompt CARE completo de Kate Moran para mensagens de erro de login]`

`[FALA]` Veja o exemplo real publicado pela própria Kate Moran na NN/G. É um prompt longo — e a autora admite: "isso dá trabalho". Mas para tarefas onde tom e estilo importam, vale.

### Bloco 4 — Limitações honestas (2 min)

`[SLIDE 8 — caveats da própria NN/G]`

`[FALA]` A própria NN/G alerta: CARE dá trabalho. Às vezes custa mais tempo do que fazer à mão. Funciona melhor para quem tem menos experiência na tarefa. E exige iteração — raramente a primeira saída está pronta.

### Bloco 5 — Exercício (1 min)

`[SLIDE 9 — exercício 6.1]`

`[FALA]` Exercício 6.1: construa um prompt CARE para um e-mail de proposta comercial. Gabarito no `exercicios.md`.

### Bloco 6 — Fechamento (1 min)

`[SLIDE 10 — ponte para Módulo 3]`

`[FALA]` Vimos 3 frameworks práticos. Agora vamos para técnicas avançadas: ReAct e BDI.

---

# Módulo 3 — Técnicas Avançadas

## Aula 7 — ReAct: raciocínio + ação

### Bloco 1 — Abertura (1 min)

`[SLIDE 1 — "e quando precisa buscar informação?"]`

`[FALA]` Até agora, os prompts operam com conhecimento interno do modelo. E quando a tarefa precisa de informação externa? Conheça ReAct.

### Bloco 2 — Definição (3 min)

`[SLIDE 2 — ReAct = Reasoning + Acting]`

`[FALA]` ReAct é um framework proposto por Yao e colegas em 2022, num paper acadêmico peer-reviewed. Combina raciocínio e ação de forma intercalada.

`[SLIDE 3 — trajetória Thought/Action/Observation]`

`[FALA]` A trajetória é: Thought (raciocínio), Action (chamada a ferramenta), Observation (resultado da ferramenta), repetir até chegar à resposta.

### Bloco 3 — Por que ReAct (2 min)

`[SLIDE 4 — CoT vs Acting vs ReAct]`

`[FALA]` Chain-of-thought raciocinha mas não acessa o mundo externo — alucina fatos. Acting puro age mas não raciocina — falha em decompor metas. ReAct pega o melhor dos dois.

### Bloco 4 — Demo (3 min)

`[MOSTRAR exemplo da trajetória do paper: pergunta sobre Colorado orogeny]`

`[FALA]` Veja o exemplo clássico do paper. O modelo raciocina ("preciso buscar X"), age (faz Search), observa (lê resultado), raciocina de novo. Cada Thought guia o próximo Action.

### Bloco 5 — Resultados empíricos (1 min)

`[SLIDE 5 — HotpotQA, Fever, ALFWorld, WebShop]`

`[FALA]` ReAct supera acting puro em todos os benchmarks. Às vezes supera CoT, às vezes fica atrás — os melhores resultados vêm de combinar ReAct + CoT + self-consistency.

### Bloco 6 — Implementação (1 min)

`[SLIDE 6 — LangChain]`

`[FALA]` Na prática, ReAct é o padrão de agente em bibliotecas como LangChain. Você não escreve a trajetória à mão — o framework orquestra.

### Bloco 7 — Exercício (1 min)

`[SLIDE 7 — exercício 7.1]`

`[FALA]` Exercício 7.1: escreva a trajetória Thought/Action/Observation para a pergunta "Qual o PIB per capita do país onde nasceu o criador do Python?". Gabarito no `exercicios.md`.

### Bloco 8 — Fechamento (1 min)

`[SLIDE 8 — diferente de frameworks práticos]`

`[FALA]` ReAct é diferente dos frameworks práticos. Tem paper acadêmico. É reproduzível. É o primeiro do curso com embasamento científico.

---

## Aula 8 — BDI: arquitetura de agentes

### Bloco 1 — Abertura (1 min)

`[SLIDE 1 — "e quando precisa de um agente com estado interno?"]`

`[FALA]` ReAct lida com tarefas que precisam de informação externa. Mas e quando precisamos simular um **agente com objetivos, crenças e planos**? Aí entra o BDI.

### Bloco 2 — Definição e origem (3 min)

`[SLIDE 2 — BDI: Belief-Desire-Intention]`

`[FALA]` BDI significa Belief, Desire, Intention. É um modelo de software para agentes racionais, proposto por Rao e Georgeff em 1995, baseado na filosofia de Michael Bratman de 1987.

`[SLIDE 3 — aviso: BDI não é framework de prompt]`

`[FALA]` Importante: BDI **não** é um framework de prompt. É um modelo de arquitetura de agentes de software. Vamos usá-lo como **analogia** para prompts, mas o uso original é outro.

### Bloco 3 — Os três componentes (3 min)

`[SLIDE 4 — Beliefs]`

`[FALA]` Beliefs: o que o agente sabe sobre o mundo. Em prompts: fatos, regras do domínio, dados do caso.

`[SLIDE 5 — Desires]`

`[FALA]` Desires: o que o agente gostaria de alcançar. Em prompts: os objetivos da tarefa.

`[SLIDE 6 — Intentions]`

`[FALA]` Intentions: o que o agente escolheu fazer — os planos concretos. Em prompts: os passos numerados que a IA deve seguir.

### Bloco 4 — Demo (3 min)

`[MOSTRAR prompt BDI para planejador financeiro (dívida vs investimento)]`

`[FALA]` Veja este exemplo. Beliefs traz os fatos econômicos (juros, inflação) + perfil do usuário. Desires traz os objetivos. Intentions traz os 5 passos concretos. Repare como a estrutura obriga o modelo a raciocinar com estado interno.

### Bloco 5 — Quando usar (1 min)

`[SLIDE 7 — quando usar BDI em prompts]`

`[FALA]` Use a analogia BDI quando a tarefa exigir um "agente com objetivos, regras internas e tomada de decisão estruturada" — assistente jurídico, planejador financeiro, tutor de idiomas.

### Bloco 6 — Exercício (1 min)

`[SLIDE 8 — exercício 8.1]`

`[FALA]` Exercício 8.1: construa um prompt BDI para um planejador financeiro. Gabarito no `exercicios.md`.

### Bloco 7 — Fechamento (1 min)

`[SLIDE 9 — resumo do Módulo 3]`

`[FALA]` Vimos ReAct (informação externa) e BDI (estado interno). São técnicas avançadas, ambas com embasamento acadêmico. No Módulo 4, vamos aprender a **avaliar** tudo isso com rúbricas.

---

# Módulo 4 — Avaliação com Rúbricas

## Aula 9 — O que é rúbrica e como construí-la

### Bloco 1 — Abertura (1 min)

`[SLIDE 1 — "como avaliar prompt sem subjetividade?"]`

`[FALA]` Como você sabe se um prompt é bom? Se a saída é boa? "Achei legal" não escala. Precisamos de rúbricas.

### Bloco 2 — Definição (2 min)

`[SLIDE 2 — definição de Popham]`

`[FALA]` Rúbrica é um instrumento de avaliação que descreve explicitamente as expectativas de desempenho. Tem critérios, descritores e níveis de desempenho.

`[SLIDE 3 — papel duplo]`

`[FALA]` Rúbrica tem papel duplo: para o professor, garante correção consistente e rápida. Para o aluno, explicita expectativas e permite autoavaliação.

### Bloco 3 — Tipos (3 min)

`[SLIDE 4 — Holística vs Analítica vs Desenvolvimento]`

`[FALA]` Três tipos. Holística: uma nota global. Analítica: avalia cada dimensão separadamente. Desenvolvimento: subtipo da analítica que mapeia modos de prática numa comunidade.

### Bloco 4 — Como criar (3 min)

`[SLIDE 5 — 5 passos de Goodrich]`

`[FALA]` Método de 5 passos: revisar modelos, listar critérios, definir graduações de qualidade, praticar em modelos, introduzir auto e heteroavaliação.

`[SLIDE 6 — roteiro operacional]`

`[FALA]` Na prática: defina objetivos, liste 3-7 critérios, escreva descritores para cada nível, defina a escala, atribua pesos, teste, compartilhe com os alunos antes da entrega.

### Bloco 5 — Anatomia visual (2 min)

`[MOSTRAR matriz analítica: linhas = critérios, colunas = níveis]`

`[FALA]` A rúbrica analítica é uma matriz. Linhas: critérios. Colunas: níveis. Cada célula: descritor observável e específico.

### Bloco 6 — Exercício (1 min)

`[SLIDE 7 — exercício 9.1]`

`[FALA]` Exercício 9.1: construa uma rúbrica analítica (3 critérios × 4 níveis) para avaliar um resumo executivo. Gabarito no `exercicios.md`.

### Bloco 7 — Fechamento (1 min)

`[SLIDE 8 — próxima aula]`

`[FALA]` Na próxima aula, vamos aplicar rúbricas especificamente a prompt engineering.

---

## Aula 10 — Rúbricas para prompt engineering

### Bloco 1 — Abertura (1 min)

`[SLIDE 1 — "rúbrica + prompt engineering = magic"]`

`[FALA]` Rúbrica é a ponte entre os frameworks que vimos (RACE, TAG, CARE) e a avaliação objetiva. Sem rúbrica, "prompt bom" é subjetivo. Com rúbrica, vira processo replicável.

### Bloco 2 — Três usos (3 min)

`[SLIDE 2 — 3 usos]`

`[FALA]` Três usos em cursos de IA. Avaliar prompts dos alunos. Avaliar saídas da IA. Avaliar competência geral do aluno.

`[SLIDE 3 — rúbrica para prompt RACE]`

`[FALA]` Primeiro exemplo: rúbrica para avaliar um prompt feito em RACE. Cada critério é um componente do framework. Role bem definido? Action com verbo ativo? Context completo? Expectation com critério mensurável?

`[SLIDE 4 — rúbrica para saída de IA]`

`[FALA]` Segundo exemplo: rúbrica para avaliar a resposta da IA. Precisão factual, aderência ao prompt, clareza, formatação, tom.

### Bloco 3 — Demo (3 min)

`[MOSTRAR a resposta do exercício 10.1 sendo avaliada na rúbrica, com cada nota justificada]`

`[FALA]` Veja a avaliação real de uma resposta. Para cada critério, justifico a nota com trecho da resposta. Isso é o que separa avaliação amadora de avaliação profissional.

### Bloco 4 — Transparência (1 min)

`[SLIDE 5 — aviso honesto]`

`[FALA]` Aviso honesto: estas rúbricas para prompt engineering são **construção didática deste curso**. Não há paper acadêmico que as valide. São aplicação prática dos conceitos de rúbrica — que são consolidados — ao domínio de prompt engineering.

### Bloco 5 — Boas práticas (1 min)

`[SLIDE 6 — boas práticas]`

`[FALA]` Boas práticas: compartilhe a rúbrica antes da entrega. Use descritores observáveis. Limite a 3-7 critérios. Teste em trabalhos-exemplo. Calibre com outros avaliadores.

### Bloco 6 — Exercício (1 min)

`[SLIDE 7 — exercício 10.1]`

`[FALA]` Exercício 10.1: aplique a rúbrica de saída de IA a uma resposta de LLM sobre um tema que você domina. Gabarito no `exercicios.md`.

### Bloco 7 — Fechamento (1 min)

`[SLIDE 8 — ponte para projeto final]`

`[FALA]` Você agora tem todas as ferramentas. No Módulo 5, vamos juntar tudo no projeto final.

---

# Módulo 5 — Projeto Final

## Aula 11 — Orientação do projeto final

### Bloco 1 — Abertura (2 min)

`[SLIDE 1 — parabéns por chegar até aqui]`

`[FALA]` Você completou 10 aulas. Agora é hora de juntar tudo num projeto final que vale 50% da sua nota.

### Bloco 2 — Escopo (5 min)

`[SLIDE 2 — o que entregar]`

`[FALA]` Você vai escolher um caso real, construir 3 prompts usando 2 frameworks diferentes, aplicar uma rúbrica e escrever uma reflexão final. Detalhes completos no arquivo `projeto-final.md`.

`[SLIDE 3 — 3 prompts]`

`[FALA]` Os 3 prompts são obrigatórios. Prompt 1 e Prompt 2: dois frameworks práticos diferentes (RACE, TAG ou CARE). Prompt 3: ReAct ou BDI.

`[SLIDE 4 — rúbrica]`

`[FALA]` Você vai escolher uma das rúbricas-exemplo do `rubrica.md`, aplicá-la a um dos seus prompts/saídas e entregar a rúbrica preenchida com justificativa.

`[SLIDE 5 — reflexão]`

`[FALA]` Reflexão final de até 300 palavras: o que funcionou, o que falhou, como você usaria rúbricas no seu dia a dia.

### Bloco 3 — Cronograma (2 min)

`[SLIDE 6 — cronograma 2 semanas]`

`[FALA]` Duas semanas, 8 horas estimadas. Semana 1: escolher caso, construir prompts 1 e 2. Semana 2: construir prompt 3, aplicar rúbrica, escrever reflexão.

### Bloco 4 — Casos sugeridos (3 min)

`[SLIDE 7 — 3 casos sugeridos]`

`[FALA]` Se você não tem um caso próprio, use um dos 3 sugeridos: e-mail de proposta comercial, resumo executivo de relatório técnico, ou microcopy de UX. Detalhes no `projeto-final.md`.

### Bloco 5 — Rúbrica de correção (3 min)

`[SLIDE 8 — rúbrica com 5 critérios]`

`[FALA]` Importante: veja a rúbrica que vou usar para corrigir vocês. 5 critérios: adequação do caso, aplicação dos frameworks, reflexão crítica, aplicação da rúbrica, qualidade da escrita. Quatro níveis. Está no `projeto-final.md`, seção 5.

`[PAUSA]`

`[FALA]` Boa prática que ensinamos: rúbrica deve ser compartilhada **antes** da entrega. Aqui está. Use-a para autoavaliar antes de enviar.

### Bloco 6 — Entrega (2 min)

`[SLIDE 9 — formato de entrega]`

`[FALA]` Entrega em arquivo único PDF ou Markdown, nome `projeto-final_[nome-aluno]`. Prazo até a Aula 12. E sim, é esperado que você use LLMs — o que está sendo avaliado é a **construção dos prompts** e a **avaliação crítica**, não a saída em si.

### Bloco 7 — Exercício (1 min)

`[SLIDE 10 — exercício 11.1]`

`[FALA]` Exercício 11.1: entregue sua proposta de caso (1 parágrafo + frameworks escolhidos + rúbrica que vai usar). Eu te dou feedback formativo antes de você seguir.

### Bloco 8 — Fechamento (1 min)

`[SLIDE 11 — você consegue]`

`[FALA]` Você tem tudo o que precisa. Mão na massa. Vejo vocês na Aula 12 para as defesas.

---

## Aula 12 — Defesa e encerramento

### Bloco 1 — Abertura (1 min)

`[SLIDE 1 — dia da defesa]`

`[FALA]` Hoje é o dia. Cada um de vocês tem 5 minutos para apresentar seu projeto.

### Bloco 2 — Roteiro da apresentação (2 min)

`[SLIDE 2 — 5 minutos divididos]`

`[FALA]` 5 minutos divididos assim: 1 minuto para o caso, 2 minutos para os prompts, 1 minuto para achados, 1 minuto para autoavaliação pela rúbrica. Treine antes — o tempo é rígido.

### Bloco 3 — Defesas (tempo variável)

`[MOSTRAR agenda das defesas]`

`[FALA]` [Defesas acontecem aqui — ao vivo ou por upload de vídeo, conforme a plataforma]

### Bloco 4 — Feedback coletivo (3 min)

`[SLIDE 3 — padrões que vi]`

`[FALA]` [Instrutor preenche em tempo real com padrões observados nas defesas — ex.: "a maioria escolheu RACE para a primeira tarefa; TAG foi subutilizado; a reflexão crítica foi o critério mais fraco"]

### Bloco 5 — Próximos passos (3 min)

`[SLIDE 4 — aprendizagem contínua]`

`[FALA]` Prompt engineering muda rápido. Para se manter atualizado: acompanhe a documentação oficial da OpenAI, Anthropic, DAIR.AI e Learn Prompting. Os links estão no `prompt-engineering.md` e no `README.md`.

`[SLIDE 5 — quando usar o que]`

`[FALA]` Resumo prático do curso inteiro numa tela: tarefa simples → TAG. Tarefa profissional com formato controlado → RACE. Tarefa com contexto rico e exemplo → CARE. Tarefa com informação externa → ReAct. Tarefa com agente e estado interno → BDI. E para avaliar tudo → rúbrica.

### Bloco 6 — Encerramento (1 min)

`[SLIDE 6 — parabéns]`

`[FALA]` Parabéns por completar o curso. O certificado está disponível na plataforma. Espero ver os prompts que vocês construírem no mundo real. Até breve.

---

## Dicas de produção para o instrutor

### Equipamento
- Câmera 1080p, microfone de lapela ou condensador
- Iluminação frontal suave
- Fundo neutro ou virtual limpo

### Slides
- Máximo 6 linhas de texto por slide
- Use o template visual do curso (cores, fontes consistentes)
- Inclua o logo do curso no canto de cada slide

### Gravação
- Grave em blocos (não aula inteira de uma vez) — facilita refazer trechos
- Pause 1-2 seg entre blocos para permitir corte limpo
- Demo em tela cheia, sem notificações (use modo não perturbe)

### Acessibilidade
- Adicione legendas (PT-BR) em todas as vídeoaulas
- Disponibilize o roteiro (este arquivo) como material complementar em PDF
- Para cada aula, referencie o arquivo `.md` de leitura complementar

### Tempo total estimado
- M1 (3 aulas × 10 min): 30 min
- M2 (3 aulas × 12 min): 36 min
- M3 (2 aulas × 12 min): 24 min
- M4 (2 aulas × 12 min): 24 min
- M5 (2 aulas × 18 min): 36 min
- **Total de vídeo:** ~2h30min (sem contar exercícios)

---

## Observação metodológica

- Os roteiros são **sugestões de fala** — o instrutor pode adaptar ao seu estilo.
- As demos sugeridas assumem acesso a um LLM (ChatGPT, Claude ou Gemini) — escolha um e seja consistente.
- Os slides sugeridos são descrições — o instrutor deve produzi-los em software (PowerPoint, Keynote, Google Slides).
- A Aula 12 (defesa) pode ser **síncrona** (ao vivo) ou **assíncrona** (aluno envia vídeo) — depende da plataforma.
- O tempo das defesas é **estimado** — ajuste conforme tamanho da turma (5 min × N alunos).