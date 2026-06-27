# Unidade 6 — BDI: arquitetura de agentes

> Curso: Prompt Engineering na Prática
> Materiais: vídeo (10-12 min) + apresentação + infográfico
> Carga horária: 2h (vídeo + leitura + 2 exercícios)

---

## 1. Objetivos de aprendizagem

Ao final desta unidade, o aluno será capaz de:

1. **Definir** o modelo BDI (Belief-Desire-Intention) e sua origem acadêmica.
2. **Explicar** por que BDI **não é** framework de prompt — e como usá-lo como analogia.
3. **Descrever** o ciclo do interpretador BDI.
4. **Construir** prompts no formato BDI (analogia) para tarefas que exigem "agente com estado interno".

---

## 2. Conteúdo

### 2.1 Definição

O **BDI (Belief–Desire–Intention)** é um modelo de software desenvolvido para a **programação de agentes inteligentes**. Ele implementa as noções filosóficas de *crença*, *desejo* e *intenção* inspirando-se na **teoria do raciocínio prático humano** de Michael Bratman (1987).

> ⚠️ **Importante:** O BDI **não é um framework de prompts**, mas um modelo arquitetural de agentes. Sua aplicação ao prompt engineering é uma **analogia pedagógica**, não o uso original do modelo.

### 2.2 Origem acadêmica

| Elemento | Detalhe |
|---|---|
| Fundamentação filosófica | Michael Bratman, *Intention, Plans, and Practical Reason* (1987) |
| Formalização em IA | Rao & Georgeff, *BDI-agents: From Theory to Practice* (ICMAS 1995) |
| Extensões formais | BDICTL (lógica modal + temporal CTL*), LORA (Wooldridge) |
| Implementações ativas em 2026 | PRS, Jason, JaCaMo, JACK, JaKtA, entre outras |

### 2.3 Os três componentes

| Sigla | Componente | Conceito | Em prompts (analogia) |
|-------|------------|----------|------------------------|
| **B** | **Beliefs** (Crenças) | O que o agente sabe/supõe sobre o mundo | Fatos, regras do domínio, dados do caso |
| **D** | **Desires** (Desejos) | Objetivos/estados que o agente gostaria de alcançar | Objetivos da tarefa |
| **I** | **Intentions** (Intenções) | Planos/compromissos de ação escolhidos | Passos concretos numerados |

**Componentes adicionais da arquitetura:**
- **Belief set / Belief base:** banco de dados de crenças.
- **Goals:** desejos adotados para perseguição ativa (devem ser consistentes).
- **Plans:** sequências de ações para alcançar intenções (podem conter sub-planos).
- **Events:** gatilhos para atividade reativa (externos ou internos).

### 2.4 Ciclo do interpretador BDI

```
1. initialize-state
2. repeat
   a. options:           option-generator(event-queue)
   b. selected-options:  deliberate(options)
   c.                    update-intentions(selected-options)
   d.                    execute()
   e.                    get-new-external-events()
   f.                    drop-unsuccessful-attitudes()
   g.                    drop-impossible-attitudes()
3. end repeat
```

**Tradução:**
1. Inicializa o estado.
2. Em loop:
   - **(a)** Gera opções a partir da fila de eventos.
   - **(b)** Delibera: seleciona quais opções perseguir.
   - **(c)** Atualiza intenções ativas.
   - **(d)** Executa próximo passo do plano.
   - **(e)** Captura novos eventos externos.
   - **(f)** Abandona intenções malsucedidas.
   - **(g)** Abandona intenções inviáveis.

### 2.5 Aplicações reais em 2026 (segundo Emergent Mind)

| Domínio | Aplicação |
|---|---|
| **Robótica** | Robôs de entrega integrando ROS com AgentSpeak/Jason |
| **Alocação em MAS** | Integração com LLMs e ASP em cadeia de suprimentos |
| **Cloud scheduling** | Agentes BDI para alocação descentralizada em datacenters |
| **Segurança** | Alert-BDI: gestão adaptativa de risco |
| **Web Semântica + LLMs** | Ontologias BDI como substrato explicável para prompt engineering |

### 2.6 Analogia ao prompt engineering

Embora o BDI não tenha sido concebido para prompts, sua lógica pode ser adaptada como **heurística** para simular um agente com objetivos e tomada de decisão estruturada:

```
[BDI — analogia para prompts]
Beliefs:    (o que a IA deve assumir como verdade/dados do domínio)
Desires:    (os objetivos que a IA deve perseguir)
Intentions: (os planos/passos concretos que a IA seguirá)
```

### 2.7 Exemplo prático — Planejador financeiro

> **Beliefs:** Você é um consultor financeiro certificado CFP. Assuma que a inflação atual está em ~4,5% ao ano, que dívidas de cartão de crédito têm juros de ~12% ao mês e que investimentos conservadores rendem ~0,8% ao mês + CDI. Considere o perfil do usuário: dívida de R$ 8.000 no cartão, reserva de R$ 3.000 guardada em poupança, renda líquida R$ 4.500/mês, gastos essenciais R$ 3.000/mês.
>
> **Desires:** (1) Recomendar a melhor alocação entre "quitar dívida" e "investir", (2) explicar o racional economicamente, (3) propor um plano de 3 meses.
>
> **Intentions:** (1) Calcular o custo financeiro de manter a dívida por mais 3 meses (juros compostos); (2) calcular o ganho alternativo de investir a reserva; (3) comparar e indicar a decisão; (4) detalhar passo a passo do plano recomendado em tópicos curtos; (5) alertar para o risco de zerar a reserva e voltar a endividar.

### 2.8 Quando usar a analogia BDI em prompts

- Tarefas que envolvem **raciocínio deliberativo** e múltiplas etapas de decisão.
- Simulação de **agentes autônomos** com objetivos, restrições e planos.
- Casos em que importa **declarar o estado do mundo** (crenças) separadamente dos objetivos (desejos).
- Exemplos: assistente jurídico, planejador financeiro, tutor de idiomas, médico diagnóstico.

### 2.9 Limitações

- É **mais complexo** que RACE/TAG/CARE — exige domínio conceitual do modelo.
- Para a maioria das tarefas cotidianas, frameworks mais simples são suficientes.
- O modelo foi pensado para **software de agentes**, não para prompts; a adaptação é uma analogia pedagógica.
- Limitações documentadas do BDI clássico: sem aprendizado nativo, lógicas subjacentes têm pouca relevância prática, sem lookahead deliberation.

### 2.10 Comparação: ReAct × CoT × BDI

| Dimensão | ReAct | Chain-of-Thought (CoT) | BDI |
|---|---|---|---|
| Origem | Yao et al., 2022 | Wei et al., 2022 | Bratman 1987; Rao & Georgeff 1995 |
| Domínio | Prompting para LLMs | Prompting para LLMs | Arquitetura de agentes de software |
| Acesso externo | ✅ Sim (tools) | ❌ Não | ✅ Via sensores/events |
| Raciocínio explícito | ✅ *Thoughts* | ✅ Passos de raciocínio | ✅ Deliberação |
| Estado interno estruturado | Implícito | Implícito | ✅ Beliefs/Desires/Intentions |
| Formalização lógica | Não | Não | ✅ BDICTL, LORA |

> **ReAct** é uma **técnica de prompt** que ressuscita, na prática, a ideia clássica de **raciocínio + ação** que o BDI formalizou teoricamente décadas antes.

---

## 3. Exercícios da unidade

### Exercício 6.1 — BDI para planejador financeiro (guiado)
Construa um prompt no formato BDI (analogia) para um planejador financeiro que deve ajudar a decidir entre pagar dívida ou investir. **Gabarito no `exercicios.md`.**

### Exercício 6.2 — BDI para caso próprio (livre)
Aplique o formato BDI a um caso do seu interesse: assistente jurídico, planejador de viagem, tutor de idiomas, etc. Entregue o prompt + saída + reflexão sobre se a analogia BDI ajudou (vs um prompt RACE simples para o mesmo caso).

---

## 4. Leitura complementar

- `docs/bdi.md` — documento base completo com 13 papers recentes, aplicações em 2026 e direções futuras

---

## 5. Fontes verificadas

1. **Wikipedia** — *Belief–desire–intention software model*. https://en.wikipedia.org/wiki/Belief%E2%80%93desire%E2%80%93intention_software_model
2. **Emergent Mind** — *Belief-Desire-Intention (BDI) Architecture* (síntese de 13 papers). https://www.emergentmind.com/topics/belief-desire-intention-bdi-architecture

### Referências acadêmicas primárias
3. **Bratman, M. E.** (1987/1999). *Intention, Plans, and Practical Reason*. CSLI Publications.
4. **Rao, A. S., & Georgeff, M. P.** (1995). *BDI-agents: From Theory to Practice*. ICMAS'95. https://www.aaai.org/Papers/ICMAS/1995/ICMAS95-042.pdf
5. **Georgeff, M. et al.** (1999). *The Belief-Desire-Intention Model of Agency*. LNCS 1555.
6. **Wooldridge, M.** (2000). *Reasoning About Rational Agents*. MIT Press.

### Papers recentes (2020-2026) citados pela síntese Emergent Mind
7. Onyedinma et al. (2020) — arXiv:2007.16089
8. Archibald et al. (2021) — arXiv:2105.02578
9. Yang et al. (2024) — arXiv:2401.02223
10. Zuppiroli et al. (2025) — arXiv:2511.17162
11. Kostka et al. (2026) — arXiv:2603.00142

> **Transparência:** BDI é o conceito com **fundamentação acadêmica mais robusta** do curso: paper seminal (Rao & Georgeff 1995), livro de referência (Bratman 1987), extensões formais (BDICTL, LORA) e implementações ativas em 2026. A analogia a prompts deve ser feita com cuidado para não deturpar o significado original.