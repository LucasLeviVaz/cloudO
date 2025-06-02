## Objetivo

O objetivo deste projeto é criar uma API RESTful, dockerizá-la e utilizá-la via em nuvem via AWS Lightsail, incluindo a configuração de um banco de dados gerenciado e controle de custos operacionais, visando não estourar o custo mensal da infraestrutura de até US$:50,00

## API

O primeiro passo foi desenvolver uma API RESTful com funcionalidades de cadastro, autenticação de usuários e consulta de dados protegidos por token JWT. Seu código foi criado utilizando PostgreSQL e testado com FastAPI.

Print do Dashboard do FastAPI conectado via máquina Nginx/LB:

![FastAPI](./imagens/fastapi_tunel.png)
/// caption
FastApi
///

Após garantir o funcionamento da api, ela foi dockerizada e sua imagem publicada no Docker Hub.

## AWS Lightsail

No AWS Lightsail, foi criado um novo serviço de container para hospedar a aplicação. No painel da plataforma, foi informado o nome da imagem hospedada no Docker Hub e configurada a porta de entrada como 8080, que é a utilizada pela API. Após o deploy do container, o Lightsail forneceu um endpoint público, que foi copiado e adicionado à documentação como URL principal da API.

Além disso, foi criado um banco de dados gerenciado do tipo PostgreSQL dentro do Lightsail. Durante a criação, foram definidos nome da instância, nome do banco, usuário e senha. Com o banco disponível, o endpoint público fornecido foi copiado e utilizado na configuração das variáveis de ambiente do container, possibilitando a conexão entre a aplicação e o banco de dados em nuvem. Após essas etapas, a API pôde ser acessada e testada com sucesso pela internet.

Print do service no Lighsail:

![Lightsail](./imagens/fast_api.png)
/// caption
Lighsail
///

## Diagrama

Diagrama do projeto:

![Lightsail](./imagens/diagrama_projeto.jpeg)
/// caption
Lighsail
///

## Como executar

Para executar basta copiar o endpoint público do container criado no Lighsail da seguinte maneira:

<!-- termynal -->

``` bash
http://fastapi-service.tkg22yejn0r8w.us-east-2.cs.amazonlightsail.com/docs
```

Link do vídeo testando utilizando FastAPI:

https://youtu.be/qDmwYlI38pM

## Custos

Print dos custos:

![Custo](./imagens/custos.png)
/// caption
Custo
///

## Conclusão

O objetivo do projeto foi alcançado com êxito, uma vez que a API desenvolvida em FastAPI foi corretamente dockerizada e implantada no serviço de containers do Amazon Lightsail, operando com sucesso em ambiente de nuvem. A aplicação demonstrou pleno funcionamento, permitindo cadastro, autenticação e consulta de dados via endpoints documentados no Swagger. Além disso, a infraestrutura foi mantida com um custo inferior a 50 dólares, atendendo aos requisitos de eficiência e viabilidade econômica estabelecidos para o projeto.