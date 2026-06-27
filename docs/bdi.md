# BDI — Belief–Desire–Intention Software Model

> Modelo de software para agentes racionais.
> Documentação de apoio para cursos online.

---

## 1. Definição

O **BDI (Belief–Desire–Intention)** é um modelo de software desenvolvido para a **programação de agentes inteligentes**. Ele implementa as noções filosóficas de *crença*, *desejo* e (em particular) *intenção* inspirando-se na **teoria do raciocínio prático humano** de Michael Bratman (1987).

Em essência, o BDI fornece um mecanismo para **separar a atividade de selecionar um plano** (a partir de uma biblioteca de planos ou de um planejador externo) **da execução dos planos atualmente ativos**. Assim, agentes BDI conseguem equilibrar o tempo gasto em *deliberar* sobre planos (escolher o que fazer) e em *executá-los* (fazer).

> ⚠️ **Importante:** O BDI **não é um framework de prompts**, mas um modelo arquitetural de agentes. Sua aplicação ao prompt engineering é uma **analogia pedagógica**, não o uso original do modelo.

---

## 2. Componentes da arquitetura

Segundo a arquitetura idealizada, um agente BDI possui os seguintes componentes:

### 2.1 Beliefs (Crenças)
Representam o **estado informacional do agente** — suas crenças sobre o mundo (incluindo ele mesmo e outros agentes). Podem conter **regras de inferência** que permitem encadeamento direto (*forward chaining*) para gerar novas crenças. Usa-se o termo *crença* (e não *conhecimento*) porque o que o agente crê **pode não ser verdadeiro** (e pode mudar no futuro).

- **Belief set / Belief base:** as crenças são tipicamente armazenadas em uma base de dados (decisão de implementação).

### 2.2 Desires (Desejos)
Representam o **estado motivacional** do agente. São objetivos ou situações que o agente *gostaria* de alcançar. Exemplos: *encontrar o melhor preço*, *ir à festa*, *ficar rico*.

- **Goals (Metas):** um *goal* é um desejo que foi adotado para perseguição ativa. O conjunto de desejos ativos deve ser **consistente** — não se pode ter, simultaneamente, os objetivos de "ir à festa" e "ficar em casa".

### 2.3 Intentions (Intenções)
Representam o **estado deliberativo** do agente — o que ele *escolheu* fazer. Intenções são desejos aos quais o agente **se comprometeu** em algum grau. Em sistemas implementados, isso significa que o agente já começou a executar um plano.

- **Plans (Planos):** sequências de ações (receitas/áreas de conhecimento) que um agente executa para alcançar uma ou mais intenções. Planos podem conter outros planos: meu plano para dirigir pode incluir um plano para encontrar as chaves do carro. Isso reflete que, no modelo de Bratman, planos são **inicialmente parciais**, com detalhes preenchidos conforme progridem.

### 2.4 Events (Eventos)
Gatilhos para atividade reativa do agente. Um evento pode atualizar crenças, disparar planos ou modificar objetivos. Podem ser **externos** (recebidos por sensores) ou **internos** (para disparar atualizações desacopladas).

---

## 3. Fundamentação acadêmica

O BDI está fundamentado na **filosofia da ação** de Michael Bratman, que identifica o **comprometimento** (*commitment*) como o fator distintivo entre desejo e intenção. Esse comprometimento leva a:

1. **Persistência temporal dos planos** (*temporal persistence*).
2. **Geração de planos adicionais** com base naqueles aos quais já está comprometido.

O modelo foi formalizado em lógica por **Anand Rao e Michael Georgeff**, resultando na **BDICTL** — uma lógica multi-modal que combina modalidades para crenças, desejos e intenções com a lógica temporal **CTL\***. Michael Wooldridge posteriormente estendeu BDICTL para definir **LORA** (*Logic Of Rational Agents*), incorporando uma lógica de ação, permitindo raciocinar não só sobre agentes individuais, mas também sobre **comunicação e interação em sistemas multiagente**.

---

## 4. O interpretador BDI

O interpretador BDI idealizado, base da linhagem **PRS** (Procedural Reasoning System) do SRI, segue este ciclo:

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

**Tradução do ciclo:**
1. Inicializa o estado do agente.
2. Em loop:
   - **(a) Opções:** gera opções a partir da fila de eventos.
   - **(b) Deliberação:** seleciona quais opções perseguir.
   - **(c) Atualização de intenções:** ajusta o conjunto de intenções ativas.
   - **(d) Execução:** executa o próximo passo do plano ativo.
   - **(e) Eventos externos:** captura novos eventos do ambiente.
   - **(f) Abandono de atitudes malsucedidas:** descarta intenções que falharam.
   - **(g) Abandono de atitudes impossíveis:** descarta intenções inviáveis.

---

## 5. Implementações conhecidas

### 5.1 BDI "puro"
- **PRS** (Procedural Reasoning System)
- **IRMA** (considerado PRS com não-reconsideração)
- **UM-PRS**, **OpenPRS**
- **dMARS** (Distributed Multi-Agent Reasoning System)
- **AgentSpeak(L)** e variantes (RT, ARTS)
- **JAM**, **JACK Intelligent Agents**, **JADEX**, **JaKtA**
- **JASON** (interpretador Java para AgentSpeak estendido)
- **GORITE**, **SPARK**, **3APL**, **2APL**, **GOAL**
- **Gwendolen** (parte do framework MCAPL)

### 5.2 Extensões e sistemas híbridos
- **JACK Teams**, **CogniTAO**, **Living Systems Process Suite**
- **Brahms**, **JaCaMo**
- **BOID** — extensão que adiciona *Obligations* (obrigações), para tratar normas e compromissos em ambientes sociais

---

## 6. Limitações e críticas (documentadas)

- **Aprendizado:** agentes BDI não possuem mecanismos nativos na arquitetura para aprender com comportamento passado e se adaptar a novas situações.
- **Três atitudes:** teóricos da decisão clássica questionam a necessidade das três; pesquisadores de IA distribuída questionam se três são suficientes.
- **Lógicas:** as lógicas multi-modais subjacentes (sem axiomatização completa e não eficientemente computáveis) têm pouca relevância prática.
- **Múltiplos agentes:** o modelo não descreve explicitamente mecanismos de interação com outros agentes ou integração em sistemas multiagente.
- **Objetivos explícitos:** a maioria das implementações BDI não tem representação explícita de objetivos.
- **Lookahead:** a arquitetura não possui (por design) deliberação com lookahead ou planejamento prospectivo — o que pode ser indesejável quando ações consomem recursos limitados, são irreversíveis ou têm efeitos colaterais.

---

## 7. Analogia ao prompt engineering

Embora o BDI não tenha sido concebido para prompts, sua lógica pode ser **adaptada como heurística** para simular um agente com objetivos e tomada de decisão estruturada:

```
[BDI — analogia para prompts]
Beliefs:    (o que a IA deve assumir como verdade/dados do domínio)
Desires:    (os objetivos que a IA deve perseguir)
Intentions: (os planos/passos concretos que a IA seguirá)
```

### Exemplo de prompt

> **Beliefs:** Você é um assistente jurídico. Considere que a legislação brasileira vigente prevê o direito do consumidor (CDC) como norma de proteção. Os fatos do caso: compra de produto com defeito, 30 dias, loja não resolveu.
>
> **Desires:** Identificar se há fundamento legal para exigir substituição do produto ou rescisão do contrato com devolução.
>
> **Intentions:** (1) Citar o dispositivo legal aplicável; (2) Avaliar prazo de arrependimento e vício do produto; (3) Recomendar conduta assertiva ao consumidor em tópicos curtos.

> **Aviso metodológico:** esta adaptação é uma **analogia pedagógica**, não o uso original do modelo BDI. O BDI é um modelo teórico formal de agentes de software, fundamentado em lógica modal e temporal.

---

## 8. Referências (verificadas)

### Fontes principais (verificadas e autoritativas)
1. **Wikipedia** — *Belief–desire–intention software model*. https://en.wikipedia.org/wiki/Belief%E2%80%93desire%E2%80%93intention_software_model — Acessado em: jun/2026. Artigo com referências primárias auditadas.
2. **Emergent Mind** — *Belief-Desire-Intention (BDI) Architecture* (síntese de 13 papers acadêmicos). https://www.emergentmind.com/topics/belief-desire-intention-bdi-architecture — Atualizado em: abr/2026. Emergent Mind é agregador acadêmico focado em arXiv que sintetiza literatura de IA.

### Referências acadêmicas primárias (citadas pelas fontes verificadas)
3. **Bratman, M. E.** (1987/1999). *Intention, Plans, and Practical Reason*. CSLI Publications. ISBN 1-57586-192-5.
4. **Rao, A. S., & Georgeff, M. P.** (1995). *BDI-agents: From Theory to Practice*. ICMAS'95, San Francisco. PDF: https://www.aaai.org/Papers/ICMAS/1995/ICMAS95-042.pdf
5. **Rao, A. S., & Georgeff, M. P.** (1991). *Modeling Rational Agents within a BDI-Architecture*. KR'91, pp. 473–484.
6. **Georgeff, M., Pell, B., Pollack, M. E., Tambe, M., & Wooldridge, M.** (1999). *The Belief-Desire-Intention Model of Agency*. Intelligent Agents V, LNCS 1555, pp. 1–10. DOI: 10.1007/3-540-49057-4_1
7. **Wooldridge, M.** (2000). *Reasoning About Rational Agents*. The MIT Press. ISBN 0-262-23213-8.
8. **Umbrello, S., & Yampolskiy, R. V.** (2021). *Designing AI for Explainability and Verifiability...*. Int. J. of Social Robotics, vol. 14, pp. 313–322. DOI: 10.1007/s12369-021-00790-w

### Papers recentes citados pela síntese Emergent Mind (2020-2026)
9. **Onyedinma et al.** (2020). *Toward Campus Mail Delivery Using BDI*. arXiv:2007.16089
10. **Archibald et al.** (2021). *Modelling and Verifying BDI Agents with Bigraphs*. arXiv:2105.02578
11. **Stringer et al.** (2020). *Adaptable and Verifiable BDI Reasoning*. arXiv:2007.11743
12. **Yang et al.** (2024). *A BDI Agent-Based Task Scheduling Framework for Cloud Computing*. arXiv:2401.02223
13. **Zuppiroli et al.** (2025). *The Belief-Desire-Intention Ontology for modelling mental reality and agency*. arXiv:2511.17162
14. **Kostka et al.** (2026). *Evaluating Theory of Mind and Internal Beliefs in LLM-Based Multi-Agent Systems*. arXiv:2603.00142
15. **Baiardi et al.** (2024). *On the external concurrency of current BDI frameworks for MAS*. arXiv:2404.10397
16. **Léveillé** (2025). *Generating Plans for Belief-Desire-Intention (BDI) Agents Using Alternating-Time Temporal Logic (ATL)*. arXiv:2509.15238

---

## 9. Aplicações práticas documentadas (segundo Emergent Mind)

A síntese do Emergent Mind mapeia aplicações reais do BDI em diversos domínios:

| Domínio | Aplicação |
|---|---|
| **Robótica** | Robôs de entrega de correio integrando ROS (sensoreamento/atuuação de baixo nível) com intérpretes AgentSpeak/Jason para o ciclo BDI de alto nível. |
| **Alocação de recursos em MAS** | Integração com LLMs e ASP em cenários de cadeia de suprimentos colaborativos; módulos BDI explícitos e Theory-of-Mind produzem melhorias mensuráveis em resultados coordenados. |
| **Agendamento em cloud** | Agentes BDI para alocação descentralizada, robusta e resiliente a falhas em datacenters, com comunicação assíncrona e revisão de planos orientada por intenções sob incerteza. |
| **Segurança e consciência situacional** | Extensão *Alert-BDI* para gestão adaptativa de risco, classificando agentes pares por responsabilidade/veracidade e ajustando intenções de alerta. |
| **Teste de interação humano-robô** | Agentes BDI aumentados com reinforcement learning automatizam geração de testes de software coverage-driven, tratando seleção de planos como MDP. |
| **Web Semântica e integração com LLMs** | Ontologias BDI fornecem substrato de raciocínio explicável e habilitam prompt engineering logic-augmented com rastreio de justificação. |

---

## 10. Direções futuras e desafios em aberto

Pesquisa contemporânea em BDI foca em:
- **Síntese automatizada e escalável de planos** (extração de estratégias via ATL, considerando observabilidade parcial e cooperação/adversarialidade multiagente).
- **Modelos de crença mais ricos** (lógicas epistêmicas/doxásticas, crenças multifacetadas, dissonância cognitiva, moderações de personalidade), com modelagem explícita de fatores sociais e institucionais em conformidade normativa.
- **Integração com sistemas neuro-simbólicos de larga escala, Web of Data e LLMs** — explorando grounding ontológico para coerência inferencial e híbridos procedurais.
- **Verificação em runtime e adaptação segura** para autonomia de longa duração e safety-critical.
- **Controle fino de concorrência e semântica de execução** em implantações MAS em larga escala.

---

## 11. Observação metodológica

O BDI tem **fundamentação acadêmica formal verificável**: paper seminal (Rao & Georgeff, 1995), livro de referência (Bratman, 1987), extensões formais (BDICTL, LORA) e múltiplas implementações de software documentadas (PRS, Jason, JACK, JaCaMo, etc.). A síntese do Emergent Mind confirma que continua sendo **paradigma ativo de pesquisa em 2026**, com aplicações em robótica, cloud, MAS e integração com LLMs. A analogia a prompts deve ser feita com cuidado para não deturpar o significado original do termo — o BDI é um **modelo de arquitetura de agentes de software**, não uma técnica de prompt.