# FONTES DE VERDADE

## Função
Este arquivo define onde o sistema deve confiar quando há divergência de informação.

Ele existe para reduzir inconsistência entre:
- memória;
- arquivos documentais;
- e estado real dos projetos.

Sem definição clara de fonte de verdade, o sistema tende a:
- duplicar estados;
- manter versões conflitantes;
- e operar com baixa confiabilidade.

---

## Problema atual

O sistema apresenta:

- inconsistência entre arquivos e realidade;
- parte relevante da informação ainda localizada na cabeça de Caio;
- documentos que nem sempre refletem o estado real dos projetos.

---

## Situação atual (de fato)

A fonte de verdade hoje é predominantemente:

👉 **híbrida, com predominância do estado real percebido por Caio**

Isso significa:
- o repositório contém estrutura e intenção;
- mas o estado confiável muitas vezes ainda depende da leitura direta de Caio sobre a realidade.

---

## Modelo adotado

O sistema deve evoluir para:

👉 **modelo híbrido controlado**

Com três níveis:

### 1. Estado real (nível primário)
- o que de fato está acontecendo no projeto
- prevalece em caso de conflito

---

### 2. Documentação no repositório (nível secundário)
- deve refletir o estado real
- é a principal fonte consultável
- precisa ser atualizada quando divergir da realidade

---

### 3. Memória informal (nível transitório)
- inclui percepções, ideias e estados não formalizados
- deve ser convertida em documentação quando relevante

---

## Regra de conflito

Quando houver divergência:

1. verificar estado real do projeto  
2. atualizar documentação para refletir esse estado  
3. evitar coexistência de versões incompatíveis  

---

## Regra de atualização

- o sistema deve preferir atualizar em vez de duplicar;
- o que foi resolvido não deve permanecer como aberto;
- o que mudou deve repercutir nos arquivos relevantes.

---

## Implicação operacional

- nenhum arquivo é confiável por si só;
- confiabilidade depende de atualização consistente;
- leitura do sistema exige atenção ao estado real.

---

## Relação com o sistema

- impacta: [[SYSTEM]]
- impacta: [[DASHBOARD-STATUS]]
- impacta: [[SPRINT]]
- aplica-se a: todos os projetos e áreas

---

## Última Atualização Confiável
2026-04-10
