# Integration Inventory

## Função

Este arquivo registra as integrações técnicas do sistema sem expor segredos.

Ele existe para:
- permitir reconstrução do sistema;
- preservar conhecimento sobre integrações;
- evitar dependência de memória humana;
- separar arquitetura de segredos.

---

## Princípio central

O repositório não guarda segredos.

O repositório guarda:
- o que existe;
- para que serve;
- onde o segredo deve estar.

---

## Integrações identificadas

### Google

- GOOGLE_API_KEY  
- GOOGLE_IMAGEN_KEY  
- GOOGLE_MAPS_API_KEY  
- GOOGLE_OAUTH_CLIENT_SECRET  
- GOOGLE_OAUTH_CLIENT_ID  

Função:
- APIs diversas (imagem, mapas, serviços gerais)
- autenticação OAuth

Observação:
- possivelmente incompleto (existem mais APIs Google)

---

### Telegram

- TELEGRAM_BOT_TOKEN  

Função:
- canal provisório de entrada do sistema

---

### GitHub

- GITHUB_TOKEN  
- GITHUB_TOKEN_CAIO_APP  

Função:
- integração com repositório
- automações e possíveis commits futuros

---

### Infraestrutura

- HETZNER_ROOT_PASS  
- CLOUDFLARE_API_TOKEN  
- CLOUDFLARE_ACCOUNT_ID  
- CLOUDFLARE_ZONE_CAIOLEITE  
- VERCEL_API_TOKEN  

Função:
- hospedagem
- DNS
- deploy

---

### Comunicação e marketing

- MAILERLITE_API_KEY  
- INSTAGRAM_USER  
- INTAGRAM_PASS  

Observação:
- possível erro de nome em INTAGRAM_PASS

---

### Vídeo, voz e avatar

- PANDA_VIDEO_API_KEY  
- ELEVENLABS_API_KEY  
- ELEVENLABS_VOICE_ID_CAIO  
- ELEVENLABS_VOICE_ID_RIQUE  
- ELEVENLABS_VOICE_ID_ENGLISH_TEACHER  
- HEYGEN_API_KEY  
- HEYGEN_AVATAR_ID_1  
- HEYGEN_AVATAR_ID_2  
- HEYGEN_AVATAR_ID_3  

Função:
- geração de mídia
- voz e avatar

---

### WhatsApp

- CAIO_WHATSAPP_NUMBER  
- CAIO_WHATSAPP_JID  

Função:
- comunicação via WhatsApp

---

### Jurídico / assinatura

- ZAPSIGN_API_TOKEN  

---

### Outros

- GOG_KEYRING_PASSWORD  
- GOG_ACCOUNT  
- MISSION_CONTROL_SHEET  

Função:
- ainda não totalmente clara → investigar

---

## Estado do inventário

Este inventário é:
- parcial;
- derivado de backup;
- sujeito a complementação.

---

## Regra de armazenamento

- valores reais devem ser armazenados fora do repositório;
- repositório guarda apenas o mapa;
- segredos devem estar em cofre seguro (ex: Kaspersky).

---

## Próximos passos

- validar se há outras chaves não capturadas;
- classificar funções de cada variável;
- migrar para novo OpenClaw de forma controlada.

---
