# PADRÕES DE ARQUIVO

## Função
Este arquivo define como os diferentes tipos de arquivos do sistema devem ser estruturados.

Ele existe para:
- garantir consistência entre arquivos;
- permitir leitura confiável por humano e IA;
- evitar estilos arbitrários;
- sustentar continuidade e expansão do sistema.

Sem padrão, a arquitetura degrada ao longo do tempo.

---

## Princípios

- estrutura deve servir à operação, não à estética;
- padrão deve ser consistente, mas não rígido;
- cada tipo de arquivo tem função própria;
- nem todo arquivo precisa de tudo, mas deve respeitar sua categoria;
- clareza com densidade é preferível a simplicidade vazia.

---

# 1. Arquivos de Projeto (`projects/`)

## Função
Representar uma iniciativa com objetivo definido e evolução ao longo do tempo.

---

## Estrutura recomendada

### 1. Contexto
- o que é o projeto
- por que existe
- qual papel cumpre no sistema

---

### 2. Estado atual
- descrição do estado real (não ideal)
- o que já existe
- o que ainda não existe

---

### 3. Status
(usar [[criterios-status]])

- estado atual do projeto:
  - ideia / planejado / em execução / bloqueado / pausado / concluído

---

### 4. Fase atual
- em que fase o projeto está dentro do ciclo de execução
- qual o objetivo dessa fase

---

### 5. Próximos movimentos
- movimentos coerentes com a fase atual
- não é lista de tarefas detalhada
- deve refletir direção, não microexecução

---

### 6. Relações
- arquivos relacionados
- áreas impactadas
- integrações relevantes

---

## Observações

- não é backlog
- não é checklist
- deve refletir estado real
- pode evoluir ao longo do tempo

---

# 2. Arquivos de Área (`areas/`)

## Função
Representar frentes contínuas da vida e operação, sem fim definido.

---

## Estrutura recomendada

### 1. Contexto
- o que a área representa
- por que é relevante

---

### 2. Estado atual
- como essa área está hoje
- sinais relevantes (bons ou ruins)

---

### 3. Dinâmicas principais
- padrões recorrentes
- comportamentos típicos
- problemas ou forças estruturais

---

### 4. Pontos de atenção
- riscos
- fragilidades
- tensões

---

### 5. Direção desejada
- para onde essa área deveria evoluir
- não como plano fechado, mas como orientação

---

### 6. Relações
- conexão com outras áreas
- impacto em projetos

---

## Observações

- não é projeto
- não tem “conclusão”
- serve mais para leitura e orientação do que execução direta

---

# 3. Arquivos de Sistema (`system/`)

## Função
Operar o sistema vivo.

---

## Estrutura

Já definida pelos próprios arquivos:
- SYSTEM → visão executiva
- PRIORITIES → hierarquia
- SPRINT → fase de execução
- OPEN-LOOPS → tensões
- DASHBOARD → leitura
- NOW → momento atual

---

## Regra
- não duplicar função entre arquivos
- cada arquivo deve cumprir seu papel específico

---

# 4. Arquivos de Referência (`reference/`)

## Função
Definir regras, padrões e integrações.

---

## Estrutura recomendada

### 1. Função
### 2. Princípios
### 3. Definições
### 4. Regras operacionais
### 5. Relações

---

## Observações

- não devem conter estado operacional
- não devem conter execução
- são base normativa do sistema

---

# 5. Arquivos de Memória (`memory/`)

## Função
Registrar informações ao longo do tempo com função de continuidade.

---

## Tipos

- decisões
- lições
- registros
- pessoas

---

## Regra

- memória deve ser funcional
- evitar acúmulo sem propósito
- atualizar quando necessário

---

# 6. Regras gerais de aplicação

- todo arquivo deve ter função clara
- evitar mistura de categorias
- atualizar em vez de duplicar
- refletir estado real sempre que aplicável
- manter relação com outros arquivos

---

# 7. Relação com o sistema

- aplica-se a: todo o repositório
- base para: consolidação de projects e areas
- complementa:
  - [[taxonomias]]
  - [[convencoes]]
  - [[criterios-status]]
  - [[fontes-de-verdade]]

---

## Última Atualização Confiável
2026-04-10
