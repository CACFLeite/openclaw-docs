# DASHBOARD — PAINEL CAIO LEITE

## Função
Este arquivo define a lógica de visualização executiva do sistema dentro do Painel Caio Leite.

Ele existe para transformar a arquitetura documental em leitura clara, rápida e confiável, permitindo:
- entender o estado do sistema;
- identificar prioridades;
- localizar bloqueios;
- e orientar decisão sem reconstruir contexto manualmente.

O dashboard não é fonte de verdade.
Ele é uma camada de leitura sobre as fontes de verdade.

---

## Princípio Central
O dashboard não mostra tudo.
Ele mostra o que importa para decidir.

Excesso de informação gera ruído.
Falta de informação gera cegueira.
O dashboard deve operar no ponto de equilíbrio.

---

## O que o Dashboard NÃO deve ser

- coleção de widgets desconectados
- painel visual sem semântica
- duplicação de dados dos arquivos
- lista de tarefas disfarçada
- interface que parece ativa, mas não governa nada

---

## O que o Dashboard deve ser

- leitura executiva do sistema
- visualização de estado real
- mapa de prioridades e bloqueios
- entrada para navegação relacional
- interface de decisão

---

## Camadas de visualização

O dashboard deve operar em quatro camadas principais:

---

### 1. Prioridade (estrutura)

Fonte:
- [[../../system/PRIORITIES]]

Função:
- mostrar a hierarquia ativa do sistema

Pergunta que responde:
👉 “o que é mais importante agora?”

---

### 2. Execução (fase atual)

Fonte:
- [[../../system/SPRINT]]

Função:
- mostrar a fase dominante
- indicar o tipo de movimento em curso

Pergunta que responde:
👉 “em que fase estamos?”

---

### 3. Estado dos projetos

Fonte:
- arquivos em `projects/`
- [[../../system/DASHBOARD-STATUS]]

Função:
- mostrar status dos projetos principais

Formato esperado:
- projeto
- status (criterios-status)
- observação curta

Pergunta que responde:
👉 “o que está andando, parado ou travado?”

---

### 4. Tensões (open loops)

Fonte:
- [[../../system/OPEN-LOOPS]]

Função:
- expor fricções reais do sistema

Pergunta que responde:
👉 “o que está puxando energia ou travando avanço?”

---

## Regras de exibição

- mostrar apenas o que é relevante para decisão
- evitar duplicação de conteúdo
- sintetizar sem perder sentido
- manter atualização coerente com fontes de verdade

---

## Navegação

O dashboard não é destino final.

Ele deve permitir:
- entrar em projetos
- abrir áreas
- acessar documentos diretamente
- navegar por relações

---

## Integração com Rique

Rique deve operar sobre o dashboard como:

- intérprete de estado
- sintetizador contextual
- orientador de decisão

Sempre considerando:
- PRIORITIES
- SPRINT
- OPEN-LOOPS
- estado dos projetos

---

## Relação com o sistema

- deriva de: [[../../system/SYSTEM]]
- lê: [[../../system/PRIORITIES]]
- lê: [[../../system/SPRINT]]
- lê: [[../../system/OPEN-LOOPS]]
- reflete: [[../../system/DASHBOARD-STATUS]]
- integra-se com: [[funcoes-rique]]

---

## Observações

- o dashboard é tão bom quanto a qualidade das fontes de verdade
- não substitui leitura profunda quando necessária
- deve ser confiável, não apenas bonito

---

## Última Atualização Confiável
2026-04-11
