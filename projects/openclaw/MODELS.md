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

## Última Atualização Confiável
2026-04-09
