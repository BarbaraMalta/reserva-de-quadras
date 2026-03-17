# Funcionalidades: Reserva de Quadras

## História de Usuário
Como morador do condomínio Cidade Jardim,  
Quero reservar uma das quadras disponíveis para um dia e horário específico da semana,  
Para realizar minhas aulas privadas de esportes ou praticar com amigos e/ou família de forma reservada.

---

## Critérios de Aceitação

### Cenário 1: Visualizar quadras disponíveis
**Dado** que estou autenticado no sistema  
**E** esteja na área de reserva de quadras  
**Quando** acessar a tela de reservas  
**Então** o sistema deve exibir as quadras que ainda estão disponíveis para a reserva naquele mês  

---

### Cenário 2: Selecionar data e horário da reserva
**Dado** que estou na área de reserva de quadras  
**E** tenha selecionado a quadra desejada  
**Quando** selecionar a data e o horário de início e término da reserva livres  
**E** confirmar a reserva  
**Então** o sistema deve registrar sua reserva com sucesso  
**E** tornar aquela data e horário indisponíveis para os demais moradores  

---

### Cenário 3: Visualizar reservas do morador
**Dado** que o morador esteja autenticado  
**Quando** acessar a aba de suas reservas  
**Então** o sistema mostrará as quadras reservadas por aquele morador  
**E** exibir os dias e horários de cada reserva  

---

### Cenário 4: Limite de reservas atingido
**Dado** que o morador tenha atingido o limite máximo de 5 reservas no mês  
**Quando** tentar realizar uma nova reserva  
**Então** o sistema deve impedir a ação  
**E** informar o motivo  

---

### Cenário 5: Cancelar reserva
**Dado** que o morador esteja autenticado  
**E** acesse a aba de suas reservas  
**E** esteja com reservas ativas em seu perfil  
**Quando** cancelar uma das reservas  
**Então** o sistema removerá a reserva do perfil do morador com sucesso  
**E** tornará a data e horário disponíveis de volta para os demais moradores  

---

### Cenário 6: Visualizar todas as reservas disponíveis
**Dado que** o administrador esteja autenticado  
**E** acesse a aba de reservas  
**Quando** selecionar a quadra que deseja verificar  
**Então** o sistema exibirá todo o histórico de reservas realizadas no mês  
