# FALLBACKS — OPENCLAW

## Função
Este arquivo governa o comportamento do sistema quando o modelo principal não está disponível ou quando a operação precisa rodar sob capacidade reduzida.

---

## Princípio Central
Fallback não é apenas trocar de modelo.
Fallback é mudar corretamente o modo de operação do sistema.

---

## Problema Atual
Quando o sistema cai para um modelo inferior sem alterar comportamento, ocorre contaminação operacional:
- simplificação excessiva;
- falsa confiança;
- perda de identidade;
- execução ruim;
- e inferência acima da capacidade real disponível.

---

## Regras Gerais de Fallback
- o sistema deve saber quando está degradado
- o sistema deve adaptar profundidade e iniciativa
- tarefas que exigem alta nuance não devem ser executadas como se nada tivesse mudado
- a comunicação sobre limitação deve ser honesta, mas útil

---

## Comportamentos Permitidos em Degradação
- classificação simples
- triagem preliminar
- sínteses curtas e de baixo risco
- organização mecânica
- alertas básicos
- encaminhamento para revisão posterior

---

## Comportamentos que Devem Ser Restritos
- inferência complexa sobre Caio
- consolidação de memória estrutural
- decisões autônomas de alto impacto
- leitura estratégica profunda
- reinterpretação de projetos sem base suficiente

---

## Relaciona-se com
- [[openclaw]]
- [[models]]
- [[crons]]
- [[watchdog]]

---

## Próximo Passo Real
Formalizar níveis de fallback e definir para cada nível:
- o que pode fazer;
- o que não pode fazer;
- como deve comunicar limitação;
- e que tipo de tarefa deve ser adiada.

---

---

## Tipos de Fallback

Fallbacks devem ser definidos para diferentes tipos de falha:

### 1. Fallback de Modelo
- indisponibilidade do modelo principal
- degradação para modelo inferior
- comportamento ajustado conforme [[models]]

---

### 2. Fallback de Tarefa
- tarefa exige capacidade não disponível
- sistema deve:
  - reduzir escopo
  - adiar execução
  - ou encaminhar para revisão

---

### 3. Fallback de Fluxo
- etapa anterior não concluída
- dependência ausente
- dado não disponível

Comportamento:
- interromper progressão indevida
- sinalizar bloqueio
- evitar inferência compensatória

---

### 4. Fallback de Infraestrutura
- falha em API externa
- erro em integração
- cron ou webhook não executado

Comportamento:
- tentar reexecução quando seguro
- degradar funcionalidade
- preservar consistência do sistema

---

### 5. Fallback de Coerência
- conflito entre memória e estado real
- inconsistência entre arquivos
- ambiguidade crítica

Comportamento:
- evitar decisão baseada em estado incerto
- priorizar validação
- não consolidar memória sob dúvida

---

### 6. Fallback de Segurança
- comportamento suspeito
- entrada potencialmente maliciosa
- uso fora do padrão esperado

Comportamento:
- reduzir autonomia
- limitar execução
- evitar ações irreversíveis
- sinalizar necessidade de validação

---

## Relação com Watchdog

A ativação de fallback depende de detecção prévia.

O sistema deve:

- detectar falha, degradação ou risco via [[watchdog]]
- classificar o tipo de problema
- aplicar o fallback correspondente

Fallback não detecta.
Fallback responde.

---

## Regra de Continuidade

Fallback não deve:

- produzir execução inconsistente
- mascarar falhas com respostas plausíveis
- manter fluxo como se não houvesse problema

Fallback deve:

- preservar integridade do sistema
- manter utilidade possível
- impedir degradação silenciosa

---

## Última Atualização Confiável
2026-04-10
