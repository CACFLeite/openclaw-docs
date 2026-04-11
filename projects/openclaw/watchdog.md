# WATCHDOG — OPENCLAW

## Função
Este arquivo governa a camada de monitoramento, detecção e acionamento de resposta do OpenClaw.

Sua função não é executar o sistema nem substituir fallbacks.
Sua função é vigiar o estado da operação, detectar degradações, identificar riscos relevantes e acionar o comportamento adequado.

O watchdog existe para impedir que o sistema:
- falhe silenciosamente;
- continue operando sob degradação sem saber disso;
- trate risco como ruído;
- ou mantenha aparência de normalidade quando sua integridade já foi comprometida.

---

## Princípio Central
O sistema precisa ser capaz de perceber quando deixou de operar de modo confiável.

Sem isso:
- fallbacks não entram na hora certa;
- modelos degradados operam como se fossem suficientes;
- fluxos quebrados continuam gerando saída;
- e a confiança no sistema se corrói sem visibilidade.

Watchdog não produz inteligência principal.
Watchdog preserva a possibilidade de confiar nela.

---

## Problema que este arquivo resolve
O OpenClaw depende de múltiplas camadas:
- modelo;
- integração;
- cron;
- bot;
- memória;
- fluxo;
- contexto operacional.

Quando uma dessas camadas falha, degrada ou é explorada, o sistema não pode depender apenas de percepção humana tardia.

É necessário haver uma camada explícita que:
- detecte falha;
- classifique severidade;
- identifique tipo de problema;
- e acione resposta proporcional.

---

## Escopo do Watchdog

O watchdog deve monitorar pelo menos cinco dimensões:

### 1. Saúde de modelo
- indisponibilidade do modelo principal
- degradação de capacidade
- erro de chamada
- latência anormal
- respostas incompatíveis com o nível esperado

---

### 2. Saúde de infraestrutura
- falha de API externa
- webhook inoperante
- cron não executado
- integração quebrada
- timeout recorrente

---

### 3. Saúde de fluxo
- etapa obrigatória não concluída
- dependência ausente
- fluxo interrompido sem tratamento
- saída produzida sem pré-condição suficiente

---

### 4. Saúde de coerência
- conflito entre memória e estado real
- conflito entre arquivos relevantes
- consolidação indevida sob ambiguidade
- repetição de estado superado como se estivesse ativo

---

### 5. Saúde de segurança
- comportamento suspeito
- entrada potencialmente maliciosa
- uso anômalo de integração
- padrão incompatível com operação normal
- risco de ação indevida ou irreversível

---

## Princípios de operação

- detectar antes de reagir;
- classificar antes de escalar;
- preservar integridade antes de preservar velocidade;
- reduzir autonomia quando a confiabilidade cair;
- não mascarar falha com aparência de funcionamento;
- não tratar risco real como mero detalhe técnico.

---

## Tipos de sinal que o Watchdog deve reconhecer

### Sinal técnico
Erro direto de execução, conexão, autenticação, timeout ou indisponibilidade.

### Sinal comportamental
Saída do sistema incompatível com o nível de capacidade, com o contexto ou com as regras de operação.

### Sinal estrutural
Quebra de pré-condição, inconsistência entre camadas ou fluxo operando sem base suficiente.

### Sinal de risco
Indício de abuso, exploração, ação maliciosa ou operação fora do padrão aceitável.

---

## Níveis de severidade

### Nível 1 — Atenção
Há desvio leve, mas sem comprometimento direto da integridade.

Exemplos:
- aumento de latência
- pequena degradação de qualidade
- erro pontual recuperável

Resposta esperada:
- registrar
- observar recorrência
- manter operação com cautela

---

### Nível 2 — Degradação
O sistema ainda opera, mas com perda relevante de confiabilidade ou capacidade.

Exemplos:
- fallback de modelo ativado
- integração oscilando
- fluxo rodando com limitação

Resposta esperada:
- sinalizar degradação
- restringir escopo
- aplicar fallback correspondente

---

### Nível 3 — Bloqueio
O sistema não deve seguir operando normalmente naquela função.

Exemplos:
- modelo principal indisponível sem substituição suficiente
- fluxo sem pré-condição crítica
- conflito grave de estado
- falha recorrente de integração essencial

Resposta esperada:
- interromper função afetada
- impedir progressão indevida
- escalar para revisão ou contingência

---

### Nível 4 — Risco crítico
Há ameaça à integridade, segurança ou confiabilidade central do sistema.

Exemplos:
- comportamento potencialmente malicioso
- ação irreversível sob incerteza
- comprometimento relevante de segurança
- operação sem controle mínimo de integridade

Resposta esperada:
- reduzir autonomia imediatamente
- bloquear ações sensíveis
- preservar logs e estado
- exigir validação explícita

---

## Regras de acionamento

Quando o watchdog detectar problema, deve:

1. identificar o tipo de problema  
2. classificar a severidade  
3. registrar o evento  
4. acionar o fallback correspondente, quando aplicável  
5. reduzir autonomia se a integridade estiver comprometida  
6. impedir continuidade automática quando houver risco relevante  

---

## Relação com fallbacks

- o watchdog detecta
- o fallback responde

O watchdog não deve tentar compensar sozinho uma falha estrutural.
Sua tarefa é perceber corretamente e acionar o regime adequado de operação.

Relaciona-se diretamente com:
- [[fallbacks]]
- [[models]]

---

## Relação com modelos

O watchdog deve reconhecer quando:
- o modelo em uso caiu de nível;
- a tarefa em execução exige mais capacidade do que a disponível;
- a saída produzida não é compatível com a qualidade esperada.

Nesses casos, deve:
- restringir escopo;
- acionar fallback;
- ou impedir execução indevida.

---

## Relação com segurança

O watchdog deve funcionar também como camada de contenção.

Isso inclui:
- detectar padrões anômalos;
- limitar autonomia em caso de suspeita;
- impedir ações irreversíveis quando houver risco;
- e priorizar integridade sobre continuidade cega.

---

## Regra de honestidade operacional

O watchdog existe para impedir mentira sistêmica.

O sistema não deve:
- parecer saudável quando está degradado;
- parecer seguro quando está vulnerável;
- parecer coerente quando há conflito relevante;
- nem parecer capaz quando a capacidade real caiu.

---

## Próximos desdobramentos documentais

Este arquivo exige, no futuro, detalhamento operacional de:
- sinais observáveis por camada;
- limiares de severidade;
- ações automáticas permitidas por nível;
- política de log, alerta e revisão.

Esses detalhamentos não precisam estar todos aqui neste momento, mas devem ser derivados desta lógica.

---

## Relaciona-se com
- [[openclaw]]
- [[models]]
- [[fallbacks]]
- [[crons]]
- [[integracoes]]
- [[../../core/SOUL]]
- [[../../core/Principios-de-Memoria-e-Execucao]]

---

## Última Atualização Confiável
2026-04-11
