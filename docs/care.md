# CARE — Context, Ask, Rules, Examples

> Framework de estruturação de prompts para IA generativa.
> Documentação de apoio para cursos online.

---

## 1. Definição

**CARE** é um acrônimo mnemônico proposto pela **Nielsen Norman Group (NN/G)** — referência internacional em pesquisa de UX — para lembrar os quatro componentes-chave que devem compor um prompt para ferramentas de IA generativa textual (como ChatGPT, Claude e Gemini).

> *"To get better results from generative-AI chatbots, write CAREful prompts. Include context, what you're asking the system to do, rules for how to do it, and examples of what you want."* — Kate Moran, NN/G

| Letra | Componente | Significado |
|-------|------------|-------------|
| **C** | **Context** | Descreva a situação (contexto, papel, projeto, público). |
| **A** | **Ask** | Solicite a ação específica que a IA deve executar. |
| **R** | **Rules** | Forneça restrições/gabaritos (tom, estilo, tamanho, o que evitar). |
| **E** | **Examples** | Demonstre o que você quer com bons e maus exemplos. |

---

## 2. Objetivo

O CARE ajuda a **escrever prompts mais cuidadosos** ("CAREful prompts") para obter melhores resultados de IA generativa. Não é necessário para toda interação — tarefas simples de busca de informação dispensam esse nível de detalhe —, mas é valioso quando se busca **saídas complexas ou específicas** que atendam a expectativas profissionais.

> ⚠️ **Observação importante:** O acrônimo "CARE" é compartilhado por outra definição concorrente (Context, Action, Result, Example), catalogada em ferramentas como o Prompt Edit. A versão da NN/G (Context, Ask, Rules, Examples) é adotada nesta documentação por ser proveniente da **fonte de maior autoridade** — NN/G é empresa de pesquisa de UX fundada por Jakob Nielsen e Don Norman, reconhecida internacionalmente. A variante alternativa é discutida na seção 10.

---

## 3. Características

| Atributo | Valor |
|---|---|
| Autoria | Kate Moran (NN/G) |
| Data de publicação | 24 de maio de 2024 |
| Nível | Iniciante |
| Domínio recomendado | Trabalho de UX (mas geral aplicável a escrita profissional) |
| Componentes | 4 (Context, Ask, Rules, Examples) |
| Ordem obrigatória | Não — "While CARE is a helpful mnemonic ... you don't always have to write prompts in this exact order" |

---

## 4. Estrutura do framework — os quatro componentes

### 4.1 Context — Descreva a situação
Estabeleça o **enquadramento** do prompt. Inclua tipos relevantes de detalhe:

- **Seu papel/experiência:** *"Sou um UX designer sênior com 15 anos de experiência"*
- **Onde atua:** *"no Canadá"*
- **Produto:** *"trabalho em um site de e-commerce"*
- **Tipo de empresa:** *"para um grande varejista internacional de óculos"*
- **Projeto atual:** *"estou desenhando a tela de login"*
- **Perfil de usuário / pesquisa:** *"nossos clientes são adultos jovens fashion-conscious"*
- **Screenshots:** anexe imagens de referência
- **Tarefa em andamento:** *"estou trabalhando numa mensagem de erro de login"*

Pergunta-guia: *"Se você estivesse falando com um novo consultor ou membro da equipe, como explicaria sua situação antes de pedir conselho?"*

### 4.2 Ask — Solicite ação específica
Esta é a **requisição** propriamente dita — fraseada como pergunta ou comando. Importa ser específico. Inclua:

- **Papel da IA:** *"Você é um UX writer focado em linguagem clara e direta"*
- **Saída desejada:** o que você quer produzir
- **Número de variações:** *"gere 15 opções de mensagens de erro"*
- **Passos:** processo que a IA deve seguir (possivelmente com **chain-of-thought prompting**)
- **Formato:** *"apresente as 5 finais em uma tabela com colunas 'mensagem' e 'justificativa'"*

### 4.3 Rules — Forneça restrições
IA generativa produz melhores resultados com **guardrails e restrições** claros sobre o que fazer e o que evitar. Tipos de regras:

- **Melhores práticas:** *"use linguagem simples; não seja engraçado; não culpe o usuário; evite voz passiva"*
- **Guia de estilo / tom de voz:** *"abordável e conversacional, mas não descuidado"*
- **Limites de produto:** *"máximo 100 caracteres; máximo 2 frases"*
- **Regras de marca:** guia de tom, terminologia, proibições

### 4.4 Examples — Demonstre o que você quer
Fornecer exemplos — **bons ou ruins** — do que você quer (ou não quer) que a IA produza ajuda a calibrar a saída. Inclua:

- **Bom exemplo:** *"Forneça sugestões construtivas para resolver o problema. Ex.: 'Adicione $12 mais para frete grátis' funciona bem porque especifica claramente o que o usuário deve fazer."*
- **Mau exemplo:** *"Evite mensagens como 'Oopsie, não conseguimos logar você.' É informal demais numa situação frustrante."*
- **Ideias existentes:** *"Nosso dev sugeriu 'Credenciais inválidas; confira seu e-mail e senha.' Soa técnico e formal demais."*

> O componente *Examples* aproxima-se da técnica **few-shot prompting**, mas a NN/G distingue: few-shot usa **pares entrada-saída** exatos; aqui basta mostrar **exemplos da saída desejada/indesejada**.

---

## 5. Quando usar o CARE

| Cenário | Adequação |
|---|---|
| Tarefas complexas ou específicas que exijam saída profissional | ✅ Adequado |
| Trabalho de UX (mensagens, microcopy, e-mails, resumos) | ✅ Adequado (caso de uso original da NN/G) |
| Escrita profissional (propostas, relatórios, comunicações) | ✅ Adequado |
| Tarefas simples de busca de informação | ❌ Desnecessário |
| Tarefas que a IA não consegue realizar bem (ex.: declarar impostos) | ❌ Inútil — a estrutura não compensa limitações do modelo |
| Quando você tem mais experiência fazendo a tarefa manualmente do que ensinando a IA | ⚠️ Pode custar mais tempo do que fazer à mão |

---

## 6. Vantagens

- **Mnemônico fácil de recordar** — 4 letras, em ordem familiar (palavra "CARE" = "cuidado").
- **Compatível com técnicas estabelecidas** — chain-of-thought (no componente Ask) e few-shot (no componente Examples).
- **Flexível na ordem** — não exige sequência rígida.
- **Autoridade de fonte** — proposto pela NN/G, organização respeitada em UX e pesquisa de usabilidade.
- **Aplicável a múltiplos domínios** — embora originalmente pensado para UX, generaliza para qualquer escrita profissional.
- **Resultado reproduzível e didático** — a própria autora publica um exemplo completo com prompt e saída obtida (GPT-4o).

---

## 7. Limitações (documentadas pela própria NN/G)

A NN/G lista explicitamente **caveats**:

1. **Exige trabalho:** *"If this seems like it's a lot of work, that's because it is."* — Com os modelos atuais (à época da publicação, maio/2024), esse nível de contexto estratégico é frequentemente necessário.
2. **Pode consumir mais tempo do que fazer manualmente** — especialmente para especialistas no assunto (ex.: a autora, escritora experiente, diz que escreveria a mensagem de erro mais rápido do que montar o prompt).
3. **Sensível ao tipo de tarefa** — tarefas pequenas e focadas rendem mais; tarefas inadequadas ao modelo não são salváveis por prompt.
4. **Exige iteração** — raramente a saída está pronta para uso direto; é preciso checar se a IA seguiu todas as instruções, pedir variações adicionais, combinar opções e refinar.
5. **Curva de aprendizado** — perceber *quando* vale o esforço é habilidade adquirida com prática.

---

## 8. Exemplo prático (adaptado de Kate Moran, NN/G)

### Cenário
UX designer de e-commerce de óculos precisa criar mensagem de erro para tela de login quando credenciais não conferem.

### Prompt CARE completo

> **Context:**
> Sou um UX designer sênior com 15 anos de experiência, trabalho em um site de e-commerce para um grande varejista internacional de óculos. Estou desenhando a tela de login, onde clientes entram para acessar detalhes da conta. Nossos clientes são adultos jovens que valorizam qualidade, autenticidade e autoexpressão.
>
> **Ask:**
> Você é um UX writer focado em linguagem clara e direta. Siga estes passos sem pular nenhum:
> 1. Gere 15 opções de mensagens de erro para login.
> 2. Revise as 15 opções segundo os critérios abaixo e selecione as 5 melhores.
> 3. Ranqueie essas 5 da melhor para a pior, com justificativa.
> 4. Apresente as 5 finais em uma tabela: mensagem na 1ª coluna, justificativa na 2ª.
>
> **Rules:**
> - Use linguagem simples.
> - Não seja engrajado ou esperto.
> - Não obscureça o significado da mensagem.
> - Ofereça soluções e recomendações.
> - Não culpe o usuário.
> - Evite voz passiva.
> - Tom de voz: abordável e conversacional, mas não descuidado.
> - Máximo 100 caracteres e 2 frases.
>
> **Examples:**
> ✓ Bom: *"Adicione $12 mais para frete grátis"* — especifica claramente a ação.
> ✗ Ruim: *"Oopsie, não conseguimos logar você"* — informal demais numa situação frustrante.
> (Ideia existente do dev: *"Credenciais inválidas; confira seu e-mail e senha"* — soa técnico/formal demais.)

### Saída esperada (trecho da tabela obtida pela autora com GPT-4o)

| Mensagem de erro | Justificativa |
|---|---|
| *Please check your email and password and try again.* | Simples, direta, dá próximo passo claro. |
| *The email or password doesn't match our records. Try again.* | Explicação clara e instrução de retentativa. |
| *The email or password you entered is invalid. Please re-enter them.* | Indicação clara do problema e solução. |
| *We couldn't log you in. Please check your email and password.* | Educada, clara, oferece próximo passo. |
| *Those credentials don't match our records. Try again.* | Clara e direta, com ação fácil de seguir. |

### Após a saída — iteração
A NN/G orienta: verifique se seguiu todas as instruções, peça mais opções, combine elementos manualmente. Ex.: adicionar hyperlink *"Try resetting your password, or contact us for help."*

---

## 9. Quando NÃO usar o CARE (orientação da própria NN/G)

- **Tarefas de busca de informação gerais** — contexto enxuto é suficiente.
- **Tarefas fora da capacidade do modelo** — prompt cuidadoso não resolve limitação técnica.
- **Tarefas que você faz mais rápido manualmente** — avalie custo/benefício realisticamente.

---

## 10. Variante concorrente (registro para fins didáticos)

Existe outra definição de CARE, divulgada por ferramentas especializadas como o **Prompt Edit** (promptedit.app), com componentes diferentes:

| Versão | C | A | R | E |
|---|---|---|---|---|
| **NN/G (esta documentação)** | Context | Ask | Rules | Examples |
| **Prompt Edit (variante)** | Context | Action | Result | Example |

A versão do Prompt Edit troca:
- **Ask → Action** (sinônimo, quase sem diferença).
- **Rules → Result** (diferente: Rules = restrições de processo; Result = descrição do formato esperado).
- **Examples → Example** (mesma ideia, no singular).

**Critério de escolha:** para material acadêmico/profissional, a **versão da NN/G deve prevalecer** por ser proveniente de fonte de maior autoridade (empresa de pesquisa reconhecida em UX) e com data/publicação verificáveis (Kate Moran, maio/2024). A variante do Prompt Edit pode ser mencionada como alternativa mnemônica.

---

## 11. Referências (verificadas)

### Fonte principal (autoritativa)
1. **Moran, K.** (2024, 24 maio). *CARE: Structure for Crafting AI Prompts*. Nielsen Norman Group. https://www.nngroup.com/articles/careful-prompts/ — Acessado em: jun/2026.
2. **Nielsen Norman Group** — Cartaz "CAREful Prompts" (PDF para impressão): https://media.nngroup.com/media/articles/attachments/CAREful_Prompts_-_Printable-2.pdf

### Variante alternativa
3. **Prompt Edit** — *CARE Framework | Context, Action, Result Guide*. https://www.promptedit.app/prompt-framework/care — Acessado em: jun/2026.

### Conceitos técnicos citados pela NN/G
4. **OpenAI** — *Custom instructions for ChatGPT*: https://openai.com/index/custom-instructions-for-chatgpt/ (recursos de contexto persistente)
5. **OpenAI** — *Memory and new controls for ChatGPT*: https://openai.com/index/memory-and-new-controls-for-chatgpt/ (memória persistente)
6. **OpenAI** — *GPT-4o* (modelo citado na autora): https://openai.com/index/hello-gpt-4o/

---

## 12. Pontos não confirmados / transparência metodológica

| Item | Status |
|---|---|
| Autoria do artigo da NN/G | ✅ Confirmado — Kate Moran, com foto e bio na NN/G |
| Data de publicação | ✅ Confirmado — 24 maio 2024 |
| Definição "CARE = Context, Ask, Rules, Examples" | ✅ Confirmado no artigo original da NN/G |
| Existência de variante "Context, Action, Result, Example" | ✅ Confirmado no Prompt Edit (mas sem paper acadêmico) |
| Status de "técnica acadêmica peer-reviewed" | ❌ **Não confirmado** — o CARE da NN/G é uma **heurística prática proposta em artigo de UX**, não um paper acadêmico. Não há revisão por pares formal. |
| Origem do acrônimo "CARE" | ⚠️ **Parcialmente confirmado** — a NN/G não reivindica explicitamente ter cunhado o acrônimo; propõe-o como mnemônico. Não foi possível determinar se o acrônimo existia antes de maio/2024. |
| Vídeo "CARE: Structure for Crafting AI Prompts" (4min) | ✅ Confirmado — disponível em https://www.youtube.com/watch?v=aeJ5fNFexhc (link retornado pela página da NN/G) |

> **Recomendação para o curso:** apresentar o CARE como **heurística mnemônica de UX**, não como técnica validada cientificamente. Embora a NN/G seja fonte de altíssima autoridade em UX/prática de design, o CARE não é uma técnica com embasamento em pesquisa peer-reviewed.