# Authority

## Finalidade

Este documento define a autoridade documental do sistema.

Seu objetivo é estabelecer, de forma explícita, qual tipo de arquivo possui precedência em caso de conflito, qual é a fonte de verdade para cada domínio de informação e quais camadas podem orientar, restringir, complementar ou derivar outras.

Sem uma regra clara de autoridade, o sistema tende a apresentar inconsistência, sobrescrita indevida, mistura de escopos, perda de previsibilidade e regressões operacionais.

## Princípio central

Cada tipo de informação deve possuir uma única fonte de verdade claramente definida.

Nenhum arquivo deve sobrescrever outro fora do seu domínio legítimo de autoridade.

A existência de um documento não autoriza sua expansão arbitrária para temas que pertençam a outra camada documental.

## Regra geral de precedência

Em caso de conflito entre documentos, prevalece o documento com maior autoridade estrutural dentro do domínio correspondente.

Quando houver conflito entre documentos de domínios diferentes, o conflito não deve ser resolvido de forma implícita ou silenciosa. Ele deve ser explicitado e corrigido na camada apropriada.

## Hierarquia de autoridade

A hierarquia documental do sistema segue, em termos gerais, esta ordem de precedência:

1. `governance/*`
2. `core/*`
3. `memory/*`
4. `context/*`
5. `priorities/*`
6. `projects/*`
7. `ops/*`
8. runtime interno, estado transitório e artefatos operacionais do OpenClaw

Essa hierarquia não significa que documentos de nível superior “substituem” o conteúdo dos inferiores em qualquer assunto. Ela significa que documentos de nível superior definem regras, limites e enquadramento estrutural que os níveis inferiores devem respeitar.

## Fonte de verdade por domínio

### Identidade do sistema
Fonte de verdade: `core/SYSTEM.md`

Esse arquivo define o que o sistema é, qual é seu propósito, qual é seu escopo e quais são seus limites gerais.

### Perfil operacional do usuário
Fonte de verdade: `core/USER.md`

Esse arquivo define apenas os aspectos estáveis, recorrentes e operacionalmente relevantes do usuário principal.

### Regras, precedência e governança
Fonte de verdade: `governance/*`

Esses arquivos definem como o sistema deve ser organizado, atualizado, interpretado e protegido contra conflitos estruturais.

### Memória consolidada
Fonte de verdade: `memory/*`

Esses arquivos concentram conhecimento persistente e reaproveitável que já passou por consolidação suficiente para deixar de ser apenas contexto transitório.

### Contexto atual e estado transitório
Fonte de verdade: `context/*`

Esses arquivos registram o estado corrente, circunstâncias temporárias, observações de momento e condições ainda sujeitas a alteração próxima.

### Prioridades vigentes
Fonte de verdade: `priorities/*`

Esses arquivos registram o que está ativo agora em termos de foco, urgência, direção ou atenção principal.

### Projetos específicos
Fonte de verdade: `projects/*`

Esses arquivos tratam de iniciativas delimitadas, com escopo, andamento, decisões, pendências e materiais associados a cada projeto.

### Procedimentos e rotinas operacionais
Fonte de verdade: `ops/*`

Esses arquivos registram modos de fazer, checklists, protocolos e rotinas operacionais.

## Regra de domínio

Cada documento deve permanecer dentro do seu domínio.

Exemplos:

- `core/USER.md` não deve absorver governança, prioridades temporárias ou detalhes de projeto.
- `core/SYSTEM.md` não deve absorver memória, backlog ou contexto transitório.
- `memory/*` não deve virar depósito de qualquer informação não classificada.
- `context/*` não deve ser tratado como memória consolidada.
- `projects/*` não deve redefinir identidade do sistema nem regras de governança.
- `ops/*` não deve se transformar em fonte de verdade sobre estratégia, identidade ou prioridades globais.

## Regra de conflito

Quando dois documentos parecerem entrar em conflito, o procedimento correto é:

1. identificar se ambos estão tratando do mesmo domínio;
2. identificar qual deles é a fonte de verdade legítima para esse domínio;
3. corrigir o documento que estiver fora de escopo;
4. registrar a estrutura correta, em vez de manter duplicidade semântica.

Conflitos não devem ser “resolvidos” por hábito, conveniência ou repetição do documento mais recente. Devem ser resolvidos por autoridade documental.

## Regra de derivação

Documentos de menor autoridade podem derivar, resumir, operacionalizar ou aplicar documentos de maior autoridade, desde que:

- não contradigam a fonte de verdade;
- não ampliem indevidamente o escopo da origem;
- não passem a competir com a camada superior;
- deixem claro que são aplicação, não redefinição.

## Regra sobre runtime e sistema interno

Arquivos internos do runtime, estados automáticos, sessões, artefatos temporários, caches, logs e estruturas internas do OpenClaw não devem ser tratados como autoridade documental de conteúdo.

Esses elementos pertencem à camada de execução, não à camada normativa do sistema.

Eles podem refletir estado operacional, mas não devem definir identidade, governança, memória consolidada ou prioridades estratégicas.

## Regra de atualização

Mudanças em arquivos de autoridade superior devem ser tratadas com maior rigor de revisão.

Quanto mais alto o nível do documento na hierarquia, maior deve ser o cuidado com:

- escopo;
- impacto estrutural;
- compatibilidade com os demais documentos;
- risco de contaminação de domínio;
- necessidade de validação humana.

## Limites deste documento

Este arquivo não define conteúdo específico de projetos, memória, contexto ou operação detalhada.

Ele define apenas a lógica de precedência, domínio e autoridade entre documentos do sistema.
