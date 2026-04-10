# CRITERIOS DE STATUS

## Função
Este arquivo define a semântica mínima de status do sistema, para evitar formulações enganosas como “pronto” quando ainda há bloqueios ativos relevantes.

---

## Princípio Central

Todo status deve dizer com clareza:
- em que nível algo está;
- o que isso significa;
- o que ainda falta;
- e o que impede avanço.

---

## Camadas de Status

### Status Estratégico
Expressa o valor ou lugar da frente no sistema.

Exemplos:
- prioritário
- ativo
- relevante
- em espera
- arquivado

### Status Operacional
Expressa a condição real de avanço da frente.

Exemplos:
- em execução
- bloqueado
- aguardando ação de Caio
- aguardando terceiro
- pronto para teste
- pronto para lançamento técnico
- pronto para lançamento comercial
- em revisão
- pausado

### Bloqueios Ativos
Lista objetiva do que impede avanço relevante agora.

### Próximo Passo Real
Indica o passo concreto mais consequente, não uma abstração genérica.

---

## Regras de Linguagem

- não usar “pronto” sem qualificador;
- não usar “finalizado” se ainda há dependência estrutural;
- não usar “lançado” para algo apenas tecnicamente concluído;
- não confundir relevância estratégica com prontidão operacional;
- não esconder bloqueios sob formulações otimistas.

---

## Exemplos Bons

- Status estratégico: prioritário
- Status operacional: bloqueado por ausência de ativos criativos
- Próximo passo real: upload dos vídeos e validação do pipeline

- Status estratégico: ativo
- Status operacional: pronto para beta fechado
- Próximo passo real: agendar teste com usuários definidos

---

## Exemplos Ruins

- “pronto”
- “quase pronto”
- “falta pouco”
- “em andamento” sem qualificação
- “lançado” sem distinguir se o lançamento é técnico, interno, beta ou comercial

---

## Última Atualização Confiável
2026-04-09
