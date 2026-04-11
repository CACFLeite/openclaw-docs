# MODELS — OPENCLAW

## Função
Este arquivo governa a política de uso de modelos do OpenClaw.

Ele existe para impedir que a escolha de modelo seja tratada apenas como detalhe técnico, quando na verdade ela altera profundamente:
- qualidade de leitura;
- profundidade analítica;
- autonomia;
- confiabilidade operacional;
- e coerência identitária do sistema.

---

## Princípio Central
Nem todo modelo suporta o mesmo tipo de operação.

A arquitetura deve reconhecer explicitamente:
- quais funções exigem modelos fortes;
- quais toleram modelos medianos;
- quais não devem rodar sob modelos fracos;
- e como o comportamento do sistema precisa mudar sob degradação.

---

## Problema Atual
O uso de modelos inferiores sem política comportamental correspondente gera:
- alucinação;
- simplificação indevida;
- perda de tom;
- baixa autonomia qualificada;
- e decisões ruins em tarefas que exigem nuance.

---

## Requisitos da Política de Modelos
- declarar modelo principal
- declarar fallback por nível
- declarar funções proibidas em modelos fracos
- declarar adaptação de comportamento por qualidade de modelo
- impedir que degradação técnica produza mentira semântica

---

## Perguntas Críticas
- Quais tarefas exigem modelo de alta capacidade?
- Quais podem operar em modo reduzido?
- Quais devem ser pausadas em contingência?
- Como o sistema deve comunicar limitação sem perder utilidade?

---

## Relaciona-se com
- [[openclaw]]
- [[fallbacks]]
- [[crons]]
- [[watchdog]]
- [[../../core/SOUL]]
- [[../../core/Principios-de-Memoria-e-Execucao]]

---

## Próximo Passo Real
Definir uma matriz mínima:
- tarefa;
- nível exigido de modelo;
- risco sob degradação;
- comportamento permitido;
- comportamento proibido.

---

---

## Níveis de Modelo

Para fins operacionais, os modelos são classificados em três níveis:

### Nível 1 — Alta Capacidade
- alta qualidade de leitura e síntese
- mantém coerência com SOUL e PRINCÍPIOS
- suporta análise complexa e decisões estruturais

---

### Nível 2 — Capacidade Intermediária
- leitura funcional, mas com perda de nuance
- maior risco de simplificação indevida
- adequado para tarefas operacionais e estruturadas

---

### Nível 3 — Baixa Capacidade
- alto risco de alucinação e distorção
- perda significativa de tom e coerência
- não confiável para decisões ou análise complexa

---

## Classes de Tarefa do OpenClaw

### Classe A — Cognitiva / Estrutural
Exemplos:
- interpretação de mensagens complexas
- definição de estratégia
- atualização de memória crítica
- decisões com impacto sistêmico

Exigência:
👉 apenas Nível 1

---

### Classe B — Operacional Qualificada
Exemplos:
- organização de informação
- síntese estruturada
- geração de conteúdo com critério
- apoio a execução com contexto

Exigência:
👉 Nível 1 ou 2 (com restrições)

---

### Classe C — Mecânica / Repetitiva
Exemplos:
- formatação
- transformação simples de dados
- execução previsível

Exigência:
👉 qualquer nível

---

## Matriz de Risco por Degradação

| Classe de tarefa | Risco em Nível 2 | Risco em Nível 3 |
|-----------------|------------------|------------------|
| Classe A        | alto             | crítico          |
| Classe B        | moderado         | alto             |
| Classe C        | baixo            | moderado         |

---

## Regras de Comportamento por Degradação

### Em Nível 2
- reduzir escopo de interpretação
- evitar decisões estruturais
- explicitar incerteza quando necessário
- manter aderência aos PRINCÍPIOS

---

### Em Nível 3
- não executar tarefas de Classe A
- limitar-se a tarefas mecânicas ou bem definidas
- evitar síntese complexa
- sinalizar limitação de capacidade

---

## Funções Proibidas em Modelos Fracos

Não devem ser executadas fora de Nível 1:

- definição de arquitetura
- decisões estratégicas
- interpretação de mensagens densas
- atualização de memória crítica
- qualquer tarefa que envolva múltiplas camadas do sistema

---

## Regra de Segurança Semântica

Degradação técnica não pode produzir:

- aparência de compreensão onde não há
- decisões com base em leitura insuficiente
- respostas confiantes sem lastro

Se o modelo não suporta a tarefa:
👉 deve limitar escopo ou recusar implicitamente pela redução de atuação

---

## Implicação para o OpenClaw

A arquitetura deve:

- direcionar tarefas ao nível adequado de modelo
- impedir execução indevida em nível insuficiente
- adaptar comportamento automaticamente sob fallback
- preservar coerência do sistema mesmo sob degradação

---

## Última Atualização Confiável
2026-04-10
