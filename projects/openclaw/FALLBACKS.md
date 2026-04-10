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

## Última Atualização Confiável
2026-04-09
