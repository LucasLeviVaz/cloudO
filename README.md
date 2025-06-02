## Navegação:

Este repositório está dividido em duas partes: documentação e código.

Para visualizar os relatórios dos roteiros e do projeto basta entrar na pasta docs.

O código do projeto está localizado na pasta site/projeto.


## Roteiros

Este projeto tem como objetivo transformar uma rede de servidores físicos em uma infraestrutura de nuvem privada, eficiente e gerenciável. A proposta envolve a implementação de diversas ferramentas e práticas modernas para otimizar o uso de recursos computacionais, automatizar processos e garantir alta disponibilidade.

As principais etapas do projeto incluem:

Virtualização e Gerenciamento de Servidores: Conversão de servidores físicos em recursos gerenciáveis via nuvem, melhorando a escalabilidade e a administração da infraestrutura.

Monitoramento com Grafana e Prometheus: Implementação de painéis de visualização e análise em tempo real para métricas e status da rede.

Implantação de Nuvem Privada com OpenStack: Configuração e utilização do OpenStack com redes SDN, automação com Juju e Terraform, além da implantação de aplicações em máquinas virtuais.

Infraestrutura como Código (IaC): Utilização do Terraform para definir, versionar e gerenciar a infraestrutura de forma repetível e segura, com foco em práticas como SLA (acordos de nível de serviço), DR (recuperação de desastres) e controle de identidade e acesso via Keystone.

Este projeto fornece uma base sólida para a compreensão e aplicação prática dos conceitos modernos de infraestrutura, automação e computação em nuvem.

## Projeto

O projeto consiste no desenvolvimento e deploy de uma API RESTful com FastAPI, PostgreSQL e Docker, hospedada em nuvem via AWS Lightsail. A aplicação permite cadastro, autenticação de usuários e consulta de dados protegidos por JWT, sendo acessível por meio de um endpoint público fornecido pela AWS.

A API foi dockerizada e sua imagem publicada no Docker Hub. No Lightsail, foi configurado um serviço de container para a aplicação e um banco de dados gerenciado PostgreSQL, com variáveis de ambiente definidas para garantir a integração entre backend e banco.

Todo o processo foi realizado com foco em manter os custos abaixo de US$ 50/mês, atendendo critérios de eficiência e viabilidade econômica. O funcionamento foi validado por meio de testes públicos via Swagger UI e vídeo demonstrativo.

