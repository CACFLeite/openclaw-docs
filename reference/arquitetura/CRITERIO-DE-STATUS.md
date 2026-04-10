# CRITÉRIOS DE STATUS

## Função
Este arquivo define a linguagem de status do sistema.

Ele existe para permitir:
- leitura consistente do estado dos projetos;
- distinção entre movimento real e aparência de movimento;
- alinhamento entre arquivos, dashboard e execução.

Status não são rótulos estéticos.  
São instrumentos de leitura e decisão.

---

## Princípios

- estado real acima de narrativa;
- status devem refletir fase concreta, não intenção;
- devem ser reutilizáveis e consistentes;
- devem permitir retorno entre estados;
- não devem inflar complexidade sem ganho real de leitura.

---

## Estados do sistema

### ⚪ Ideia
- ainda não estruturado
- sem execução iniciada
- pode ou não virar projeto

---

### 🔵 Planejado
- já estruturado minimamente
- possui direção clara
- ainda não entrou em execução real

---

### 🟡 Em execução
- há ação concreta acontecendo
- pode estar em validação, construção ou tentativa ativa

---

### 🔴 Bloqueado
- não avança por impedimento ativo
- há tentativa ou intenção de avanço, mas algo impede

Exemplos:
- problema técnico
- dependência externa
- falta de recurso crítico

---

### 🟣 Pausado
- não está sendo executado por decisão ou contexto
- não há tentativa ativa de avanço

Diferença-chave:
- **bloqueado** → quer andar, mas não consegue  
- **pausado** → não está tentando andar agora  

---

### 🟢 Concluído
- atingiu o critério de conclusão definido
- não depende mais de execução contínua

---

## Observações importantes

- um projeto pode voltar de qualquer estado para outro
- conclusão não impede reabertura
- execução não significa progresso real (depende de validação)
- bloqueio mal identificado gera ação errada

---

## Uso correto

- status deve ser atribuído com base no estado real
- evitar usar “em execução” como padrão automático
- revisar status quando houver mudança relevante
- não manter estados desatualizados por inércia

---

## Relação com o sistema

- alimenta: [[DASHBOARD-STATUS]]
- dialoga com: [[SPRINT]]
- aplicado em: projetos e áreas

---

## Última Atualização Confiável
2026-04-10
