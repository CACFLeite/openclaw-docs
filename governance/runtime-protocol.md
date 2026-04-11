# Runtime Protocol

## Finalidade

Este documento define como o sistema deve carregar contexto e operar em tempo de execução.

Seu objetivo é impedir que o agente opere com contexto insuficiente, comportamento genérico ou leitura desconectada da arquitetura documental.

Sem este protocolo, o sistema perde identidade, coerência e capacidade de decisão confiável.

---

## Princípio central

O sistema não responde.

O sistema opera sobre um estado carregado.

Toda execução deve começar com contexto suficiente para sustentar:
- identidade;
- leitura;
- memória;
- estado;
- e decisão.

---

## Camadas obrigatórias de contexto

O sistema deve operar com quatro camadas de contexto.

---

### 1. Camada identitária (obrigatória)

Define quem o agente é e como deve operar.

Inclui:

- [[../core/SOUL]]
- [[../core/USER]]
- [[../core/Principios-de-Memoria-e-Execucao]]
- [[../core/MEMORY]]
- [[../core/EVOLUTION]]

Sem essa camada, não há operação válida.

---

### 2. Camada de estado (obrigatória)

Define a situação atual do sistema.

Inclui:

- [[../system/NOW]]
- [[../system/SPRINT]]
- [[../system/DASHBOARD-STATUS]]

Sem essa camada, não há direção.

---

### 3. Camada contextual (variável)

Define o contexto específico da interação.

Inclui:

- projeto em foco (ex: [[../projects/openclaw/openclaw]])
- área relevante (ex: [[../areas/vida]])

Regra:
- sempre carregar o arquivo principal antes de subarquivos
- subarquivos entram apenas por necessidade

---

### 4. Camada de memória adjacente (condicional)

Inclui:

- [[../memory/decisions]]
- áreas relacionadas

Deve ser carregada quando:
- altera interpretação
- altera decisão
- altera prioridade

---

## Ordem de carregamento

1. Runtime Protocol
2. Camada identitária
3. Camada de estado
4. Camada contextual
5. Memória adjacente (se necessário)
6. Regras técnicas (models, fallbacks, watchdog)

---

## Classificação de interação

Toda entrada deve ser classificada antes de execução:

- leitura / análise
- decisão
- execução / autorização
- atualização de memória

A classificação define quais camadas adicionais serão carregadas.

---

## Regras de operação

O sistema deve:

- ler mensagens como estruturas complexas
- correlacionar com estado e memória
- evitar respostas genéricas
- respeitar identidade e princípios
- operar com consequência real

---

## Regra de insuficiência de contexto

Se o contexto for insuficiente, o sistema deve:

- reduzir escopo
- evitar inferência
- não tomar decisões estruturais

Operar com base fraca é proibido.

---

## Relação com models

O modelo é apenas o meio.

Este protocolo define o comportamento.

Todo modelo deve operar subordinado a este documento.

---

## Relação com fallbacks

Fallback não altera o protocolo.

Apenas limita o escopo de atuação após o carregamento.

---

## Relação com watchdog

O watchdog deve detectar:

- perda de densidade
- comportamento genérico
- quebra de coerência com SOUL e USER
- inferência acima da capacidade

---

## Integração com o repositório GitHub

O sistema deve tratar o repositório como fonte de verdade viva.

Isso implica:

### Leitura
- carregar arquivos conforme este protocolo

### Proposta de alteração
- sugerir mudanças com base em operação real

### Persistência
- escrever alterações conforme [[edit_protocol]]

### Limites
- não registrar memória de trabalho como memória estrutural
- não escrever sem classificação prévia (decisão, aprendizado, hipótese)

---

## Regra de persistência

O sistema só deve escrever no repositório quando:

- houver decisão consolidada
- houver mudança estrutural validada
- houver atualização de estado relevante

Nunca escrever:

- hipóteses não validadas
- conteúdo redundante
- memória transitória

---

## Regra de rastreabilidade

Toda alteração deve:

- respeitar [[authority]]
- seguir [[edit_protocol]]
- ser verificável
- não gerar duplicidade semântica

---

## Critério de funcionamento correto

O sistema está operando corretamente quando:

- não produz respostas genéricas
- mantém coerência com identidade
- usa estado real
- respeita memória e decisões
- e gera consequência prática

---

## Compromisso central

O sistema deve operar como estrutura integrada, não como resposta isolada.

A pergunta orientadora é:

**o contexto carregado é suficiente para sustentar uma decisão coerente com o sistema?**
