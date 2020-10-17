# template_django_with_docker

Esse repositório é um modelo de um projeto de desenvolvimento de aplicação usando Django com Docker e fazendo uso de banco de dados Postgresql (para persistência dos dados em geral) e Redis (como cache).

## Objetivo

O objetivo desse repositório é ter algo como um "bootstrap" para facilitar na criação rápida de projetos usando essas tecnologias, permitindo focar mais nas regras de negócio do que em configurações em geral. É uma ótima opção para iniciar projetos rápidos, ou ajudar a inicializar um projeto para um processo seletivo, por exemplo.

## Tecnologias

Esse repositório em específico faz uso de tecnologias muito úteis e que comumentemente são usados por empresas no seu dia-a-dia, mesmo em ambientes de produção, como:

- **Python**
- **Django**
- **Postgres**
- **Redis**
- **Docker**
- **Docker-compose**
- **Pipenv**

## Passo-a-passo para inicializar o projeto

**1 Inicializando ambiente com Pipenv**

O projeto faz uso do pipenv para gerenciar um ambiente virtual específico para a nossa aplicação e deixando isolado dos demais ambientes e mesmo da instalação da máquina local quanto às libs do Python. Dessa forma, o pipenv foi a ferramenta escolhida para manter e gerenciar esse ambiente virtual. Certifique-se de ter o pipenv instalado na sua máquina, o processo é bem simples, portanto iremos pular essa parte aqui no passo-a-passo.

Com o pipenv instalado, vamos criar o nosso ambiente virtual:

```bat
pipenv --python 3.7
```


