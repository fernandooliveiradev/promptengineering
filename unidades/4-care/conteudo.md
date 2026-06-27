# Unidade 4 — Framework CARE

> Curso: Prompt Engineering na Prática
> Materiais: vídeo (10-12 min) + apresentação + infográfico
> Carga horária: 2h (vídeo + leitura + 2 exercícios)

---

## 1. Objetivos de aprendizagem

Ao final desta unidade, o aluno será capaz de:

1. **Definir** o framework CARE (versão Nielsen Norman Group) e seus 4 componentes.
2. **Explicar** por que adotamos a versão da NN/G e não a do Prompt Edit.
3. **Construir** prompts CARE completos, incluindo exemplos (bons e maus).
4. **Reconhecer** as limitações documentadas pela própria NN/G.

---

## 2. Conteúdo

### 2.1 Definição

**CARE** é um acrônimo mnemônico proposto pela **Nielsen Norman Group (NN/G)** para lembrar os quatro componentes-chave que devem compor um prompt para IA generativa.

> *"To get better results from generative-AI chatbots, write CAREful prompts. Include context, what you're asking the system to do, rules for how to do it, and examples of what you want."* — Kate Moran, NN/G

| Letra | Componente | Significado |
|-------|------------|-------------|
| **C** | **Context** | Descreva a situação (contexto, papel, projeto, público). |
| **A** | **Ask** | Solicite a ação específica que a IA deve executar. |
| **R** | **Rules** | Forneça restrições/gabaritos (tom, estilo, tamanho, o que evitar). |
| **E** | **Examples** | Demonstre o que você quer com bons e maus exemplos. |

### 2.2 Características

| Atributo | Valor |
|---|---|
| Autoria | Kate Moran (NN/G) |
| Data de publicação | 24 de maio de 2024 |
| Nível | Iniciante |
| Domínio recomendado | UX (original) + escrita profissional em geral |
| Componentes | 4 |
| Ordem obrigatória | Não — "you don't always have to write prompts in this exact order" |

### 2.3 Por que adotamos a versão NN/G (importante!)

⚠️ **Aviso:** existe **mais de uma definição de CARE** no mercado.

| Versão | C | A | R | E |
|---|---|---|---|---|
| **NN/G (esta unidade)** | Context | Ask | Rules | Examples |
| **Prompt Edit (variante)** | Context | Action | Result | Example |

**Critério de escolha:** a **NN/G é a fonte de maior autoridade** — empresa de pesquisa de UX fundada por Jakob Nielsen e Don Norman, reconhecida internacionalmente. O artigo foi publicado em maio/2024 por Kate Moran. Para um curso acadêmico/profissional, a versão da NN/G deve prevalecer.

### 2.4 Os 4 componentes explicados

**C — Context (descreva a situação):**
Estabeleça o enquadramento do prompt. Inclua tipos relevantes de detalhe:
- Seu papel/experiência: *"Sou um UX designer sênior com 15 anos de experiência"*
- Onde atua: *"no Canadá"*
- Produto: *"trabalho em um site de e-commerce"*
- Tipo de empresa: *"para um grande varejista internacional de óculos"*
- Projeto atual: *"estou desenhando a tela de login"*
- Perfil de usuário / pesquisa: *"nossos clientes são adultos jovens fashion-conscious"*
- Screenshots: anexe imagens de referência

> Pergunta-guia: *"Se você estivesse falando com um novo consultor, como explicaria sua situação antes de pedir conselho?"*

**A — Ask (solicite ação específica):**
Esta é a requisição propriamente dita. Inclua:
- Papel da IA: *"Você é um UX writer focado em linguagem clara"*
- Saída desejada: o que produzir
- Número de variações: *"gere 15 opções"*
- Passos: processo numerado (pode usar **chain-of-thought prompting**)
- Formato: *"apresente as 5 finais em uma tabela"*

**R — Rules (forneça restrições):**
IA generativa produz melhores resultados com guardrails. Tipos de regras:
- Melhores práticas: *"use linguagem simples; não seja engrajado; não culpe o usuário"*
- Guia de estilo / tom de voz: *"abordável e conversacional, mas não descuidado"*
- Limites de produto: *"máximo 100 caracteres; máximo 2 frases"*

**E — Examples (demonstre o que você quer):**
Forneça exemplos — bons ou ruins — do que você quer (ou não quer). Inclua:
- Bom exemplo: *"Forneça sugestões construtivas. Ex.: 'Adicione $12 mais para frete grátis' funciona bem porque especifica a ação."*
- Mau exemplo: *"Evite 'Oopsie, não conseguimos logar você.' É informal demais numa situação frustrante."*

> O componente *Examples* aproxima-se da técnica **few-shot prompting**, mas a NN/G distingue: few-shot usa pares entrada-saída exatos; aqui basta mostrar exemplos da saída desejada/indesejada.

### 2.5 Quando usar o CARE

| Cenário | Adequação |
|---|---|
| Tarefas complexas ou específicas que exijam saída profissional | ✅ Adequado |
| Trabalho de UX (mensagens, microcopy, e-mails, resumos) | ✅ Adequado (caso original da NN/G) |
| Escrita profissional (propostas, relatórios, comunicações) | ✅ Adequado |
| Tarefas simples de busca de informação | ❌ Desnecessário |
| Tarefas que a IA não consegue realizar bem | ❌ Inútil |
| Quando você tem mais experiência fazendo a tarefa manualmente | ⚠️ Pode custar mais tempo |

### 2.6 Limitações (documentadas pela própria NN/G)

1. **Exige trabalho:** *"If this seems like it's a lot of work, that's because it is."*
2. **Pode consumir mais tempo que fazer manualmente** — especialmente para especialistas.
3. **Sensível ao tipo de tarefa** — tarefas pequenas rendem mais; inadequadas ao modelo não são salváveis.
4. **Exige iteração** — raramente a saída está pronta; é preciso checar, pedir variações, refinar.
5. **Curva de aprendizado** — perceber quando vale o esforço é habilidade adquirida.

### 2.7 Exemplo prático (Kate Moran, NN/G)

#### Cenário
UX designer de e-commerce de óculos precisa criar mensagem de erro para tela de login quando credenciais não conferem.

#### Prompt CARE completo

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

#### Saída esperada (trecho, obtida pela autora com GPT-4o)

| Mensagem de erro | Justificativa |
|---|---|
| *Please check your email and password and try again.* | Simples, direta, dá próximo passo claro. |
| *The email or password doesn't match our records. Try again.* | Explicação clara e instrução de retentativa. |

---

## 3. Exercícios da unidade

### Exercício 4.1 — CARE para proposta comercial (guiado)
Construa um prompt CARE (versão NN/G) para um e-mail de **proposta comercial** a um cliente potencial. **Gabarito no `exercicios.md`.**

### Exercício 4.2 — CARE para problema difícil (livre)
Construa um prompt CARE para uma tarefa em que você já tenha dificuldade com IA generativa. Entregue: prompt + saída + reflexão (1 parágrafo) sobre se o CARE resolveu o problema.

---

## 4. Leitura complementar

- `docs/care.md` — documento base completo, com variante Prompt Edit registrada e referências

---

## 5. Fontes verificadas

1. **Moran, K.** (2024, 24 maio). *CARE: Structure for Crafting AI Prompts*. Nielsen Norman Group. https://www.nngroup.com/articles/careful-prompts/
2. **NN/G** — Cartaz "CAREful Prompts" (PDF): https://media.nngroup.com/media/articles/attachments/CAREful_Prompts_-_Printable-2.pdf
3. **Prompt Edit** — CARE (variante alternativa): https://www.promptedit.app/prompt-framework/care

> **Transparência:** O CARE da NN/G é uma **heurística prática proposta em artigo de UX**, não paper peer-reviewed. A NN/G é fonte de altíssima autoridade em UX, mas o CARE não é técnica cientificamente validada.