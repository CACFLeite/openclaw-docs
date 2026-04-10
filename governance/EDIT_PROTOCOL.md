# Edit Protocol

## Finalidade

Este documento define o protocolo obrigatório para criação, edição, substituição e validação de arquivos no sistema.

Seu objetivo é garantir consistência, previsibilidade, auditabilidade e evitar regressões, perda de conteúdo ou corrupção estrutural.

## Princípio central

Nenhuma edição estrutural deve ser feita sem:

1. definição clara do objetivo da alteração;
2. compreensão do escopo do arquivo;
3. validação posterior do resultado.

## Tipos de edição

### Substituição completa

Deve ser usada quando:

- o arquivo está contaminado;
- o escopo foi violado;
- a estrutura precisa ser redefinida.

Regras:

- substituir o arquivo inteiro;
- não misturar conteúdo antigo com novo;
- validar imediatamente após salvar.

### Edição parcial

Deve ser usada quando:

- a estrutura geral está correta;
- apenas trechos específicos precisam de ajuste.

Regras:

- alterar apenas o necessário;
- não reescrever o arquivo inteiro sem motivo;
- evitar mudanças colaterais.

### Criação de novo arquivo

Deve ser usada quando:

- o conteúdo pertence a um novo domínio;
- o escopo não se encaixa em arquivos existentes.

Regras:

- respeitar a estrutura de pastas;
- definir claramente o propósito do arquivo;
- evitar duplicidade de função.

## Validação obrigatória

Após qualquer edição, deve-se validar:

- se o arquivo foi salvo corretamente;
- se o conteúdo corresponde ao esperado;
- se não houve perda de formatação;
- se não houve truncamento;
- se o arquivo continua coerente com sua finalidade.

## Protocolo de verificação

Sempre que possível:

- ler início do arquivo;
- ler final do arquivo;
- confirmar estrutura geral;
- validar pontos críticos.

## Regra de não confiança

Nenhum sistema automatizado deve ser considerado confiável para escrita sem validação.

Confirmações de sucesso não substituem verificação direta.

## Regra de consistência

Arquivos não devem:

- misturar escopos;
- assumir funções de outros documentos;
- crescer de forma descontrolada;
- acumular conteúdo sem organização.

## Regra de rollback

Antes de alterações críticas:

- manter uma versão anterior;
- permitir retorno rápido em caso de erro.

## Regra de clareza

Edições devem priorizar:

- clareza estrutural;
- legibilidade;
- organização lógica;
- facilidade de revisão futura.

## Limites

Este protocolo não define:

- conteúdo específico dos arquivos;
- estrutura de domínio;
- prioridades do sistema.

Ele define apenas como mudanças devem ser feitas.
