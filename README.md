# Cloud Gateway

O Cloud Gateway é uma ponte que padroniza o acesso aos microserviços a partir de uma URL única.
<hr/>
<img width="483" height="161" alt="image" src="https://github.com/user-attachments/assets/39ad5396-662e-43e3-ae20-2ab1cd1f86f1" />
<hr/>

Como mostrado na imagem, cada microserviço possui uma porta específica e com o gateway podemos centralizar todas as requisições à um único caminho,
facilitando toda a comunicação com Client-Server sem que o cliente precise especificar a porta para qual microserviço ele deseja se comunicar.

## Vantagens
- URL única e padrão para todos os microserviços.
- Praticidade em adicionar métodos de segurança, como OAuth2 ou JWT.

## Keycloak

Nessa implementação do Cloud Gateway, utilizei o Keycloak para o gerenciamento da segurança com OAuth2. Em cada requisição o cliente possui um token com duração de 10 minutos
e gerado a partir de um secret definido no Keycloak.

## Tecnologias
- Java 17
- Spring Boot 3
- Spring Cloud
- Eureka Discovery Client
- Spring Webflux
- OAuth2 Resource Server
- Keycloak
