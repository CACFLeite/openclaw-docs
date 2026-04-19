# GRAPH_MODEL

## Função

Este documento define o modelo de dados do grafo cognitivo do sistema.

Ele estabelece:

- tipos de nós  
- tipos de relações  
- estrutura dos dados  
- regras de consistência  

Sem um modelo claro, o grafo se torna ruído.

---

## Princípio central

O grafo não representa tudo.

O grafo representa apenas:

👉 aquilo que altera a estrutura de compreensão, decisão ou vida ao longo do tempo

---

## Tipos de nós (Node Types)

### 1. Projeto
- iniciativas estruturadas  
- ex: OpenClaw, Painel Caio Leite  

---

### 2. Decisão
- escolhas relevantes  
- alteram direção  

---

### 3. Evento de vida
- acontecimentos com impacto real  
- ex: adoção, perdas, mudanças  

---

### 4. Aprendizado
- mudanças de compreensão  
- refinamentos cognitivos  

---

### 5. Padrão
- recorrência detectada  
- comportamento repetido  

---

### 6. Erro recorrente
- falhas que se repetem  
- pontos de atenção estrutural  

---

### 7. Tensão
- conflitos ativos  
- fricções do sistema  

---

### 8. Hipótese
- interpretação ainda não validada  
- deve ter baixa autoridade  

---

## Estrutura de um nó

Cada nó deve conter:

```json id="y9z0kg"
{
  "id": "string_unico",
  "tipo": "projeto | decisao | evento | aprendizado | padrao | erro | tensao | hipotese",
  "descricao": "texto claro e objetivo",
  "data_criacao": "YYYY-MM-DD",
  "estado": "ativo | resolvido | arquivado",
  "relevancia": "baixa | media | alta | estrutural",
  "origem": "conversa | execucao | input_humano",
  "validacao": "ia | humano",
  "tags": []
}
