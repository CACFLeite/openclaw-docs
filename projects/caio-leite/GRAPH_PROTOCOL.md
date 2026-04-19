# GRAPH_PROTOCOL

## Função

Este documento define como o sistema deve interpretar interações e decidir quando, como e o que estruturar no grafo cognitivo.

Ele regula o comportamento da IA na transição entre:

- conversa → memória  
- memória → estrutura (grafo)  

Sem este protocolo, o grafo tende a inflar, perder relevância e se tornar inutilizável.

---

## Princípio central

A IA não constrói o grafo automaticamente.  
A IA propõe estruturação.

O grafo é construído por:

👉 interpretação da IA + curadoria humana

---

## Etapas do processamento

Toda interação deve seguir:

### 1. Leitura
Interpretar a mensagem em contexto.

---

### 2. Classificação

Classificar o conteúdo em:

- trivial  
- contextual  
- relevante  
- estrutural  

---

### 3. Decisão de persistência

- trivial → descartar  
- contextual → manter local  
- relevante → memória  
- estrutural → candidato a nó  

---

### 4. Proposta de estruturação

Se estrutural:

- sugerir criação de nó  
- sugerir tipo  
- sugerir relações  

---

### 5. Validação

- estrutural → validação humana obrigatória  
- relevante → pode seguir com menor rigor  
- hipótese → marcar como não validada  

---

### 6. Persistência

Após validação:

- criar nó  
- criar relações  
- atualizar grafo  

---

## Regra de criação de nós

Criar nó apenas quando houver:

- impacto real  
- mudança de direção  
- recorrência  
- aprendizado significativo  
- evento de vida relevante  

---

## Regra de não criação

Não criar nó para:

- eventos do dia a dia  
- tarefas operacionais  
- pequenas frustrações  
- variações emocionais momentâneas  

---

## Regra de sugestão

A IA deve:

- sugerir criação de nó quando detectar relevância  
- explicar de forma objetiva  
- classificar nível de impacto  

---

## Regra de silêncio estrutural

A IA deve **não sugerir nada** quando:

- não houver impacto real  
- o evento for trivial  
- a estrutura não agregaria valor  

---

## Regra de relações

A IA deve sugerir relações quando:

- há dependência clara  
- há causa e efeito  
- há influência relevante  
- há evolução temporal  

---

## Regra de não excesso de relações

Evitar:

- conectar tudo com tudo  
- criar relações fracas  
- criar relações genéricas  

---

## Regra de atualização

Ao receber nova informação:

- atualizar nó existente se aplicável  
- evitar duplicação  
- fundir conceitos semelhantes  

---

## Regra de ciclo de vida

Todo nó deve evoluir:

- ativo → resolvido → arquivado  

A IA deve sugerir mudanças de estado quando:

- um problema foi resolvido  
- uma decisão foi superada  
- um padrão deixou de existir  

---

## Regra de hipótese

Hipóteses:

- devem ser marcadas como tal  
- não devem ser tratadas como verdade  
- não devem virar estrutura sem validação  

---

## Regra de compressão

Quando houver:

- múltiplos nós similares  
- redundância  
- sobreposição  

A IA deve sugerir:

- fusão  
- simplificação  
- reorganização  

---

## Regra de relevância temporal

A IA deve considerar:

- impacto ao longo do tempo  
- não apenas relevância momentânea  

---

## Regra de intervenção humana

A IA deve acionar validação quando:

- impacto é estrutural  
- envolve identidade ou vida pessoal  
- altera direção relevante  

---

## Regra de não autonomia total

A IA não deve:

- criar grafo completo automaticamente  
- assumir decisões estruturais  
- substituir julgamento humano  

---

## Relação com memória

- memória alimenta o grafo  
- grafo é camada mais seletiva  

---

## Relação com execução

- execução pode gerar nós  
- mas nem toda execução vira estrutura  

---

## Anti-padrões

Evitar:

- inflar o grafo  
- criar nós genéricos  
- criar relações fracas  
- transformar tudo em estrutura  
- ignorar validação humana  

---

## Critério de funcionamento correto

O sistema está correto quando:

- poucos nós, mas relevantes  
- relações claras  
- evolução ao longo do tempo  
- ausência de ruído  

---

## Compromisso central

O protocolo deve garantir que:

- o grafo represente evolução real  
- a IA não gere poluição estrutural  
- a curadoria humana preserve qualidade  

Pergunta orientadora:

**isso merece fazer parte da estrutura da minha evolução ao longo do tempo ou é apenas um evento passageiro?**
