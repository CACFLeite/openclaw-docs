# ARCHITECTURE_MVP — Cognitive Graph Engine

## Função

Este documento define a arquitetura técnica mínima (MVP) para colocar o Cognitive Graph Engine funcionando integrado ao OpenClaw.

Objetivo do MVP:
👉 sair do zero → sistema funcional simples → evoluir depois

---

## Princípio central

Primeiro funcionar.  
Depois escalar.

Não usar:
- banco complexo
- UI complexa
- múltiplos serviços desnecessários

---

## Componentes do MVP

O sistema terá 4 partes:

---

### 1. Parser de entrada

Responsável por:

- receber texto (conversa, decisão, input)
- enviar para análise do Rique

Formato:

```json
{
  "input": "texto da conversa",
  "context": "projeto ou geral"
}
