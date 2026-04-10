# CRONS — OPENCLAW

## Função
Este arquivo governa a leitura e avaliação dos crons do OpenClaw como parte da operação real do sistema.

---

## Princípio Central
Cron não é apenas automação técnica.
Cron é um agente operacional recorrente e, portanto, precisa de governança semântica, confiabilidade e escopo adequado.

---

## Problema Atual
Há crons ativos úteis, mas parte deles:
- depende excessivamente de LLM para lógica sensível;
- pode operar com modelo inadequado;
- sofre com falhas de provider ou billing;
- e nem sempre está integrado a uma arquitetura de autoridade documental clara.

---

## Crons Conhecidos
- monitoramento de e-mails
- watchdog
- daily briefing
- fechamento diário
- lembrete 17h
- monitor de saúde
- DNUS 45 dias
- pesquisa OpenClaw
- radar de oportunidades

---

## Perguntas Críticas
- Quais crons geram valor real recorrente?
- Quais crons estão só produzindo ruído?
- Quais crons dependem de modelos fortes?
- Quais crons deveriam ser rebaixados para tarefas mais mecânicas?
- Quais crons precisam ser desligados até reconstrução?

---

## Relaciona-se com
- [[openclaw]]
- [[models]]
- [[fallbacks]]
- [[watchdog]]
- [[integracoes]]

---

## Próximo Passo Real
Auditar cada cron com os campos:
- função;
- frequência;
- dependência de modelo;
- risco operacional;
- valor real;
- estado atual;
- decisão: manter, revisar, pausar ou encerrar.

---

## Última Atualização Confiável
2026-04-09
