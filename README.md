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

### 1. Inicializando ambiente com Pipenv

O projeto faz uso do pipenv para gerenciar um ambiente virtual específico para a nossa aplicação e deixando isolado dos demais ambientes e mesmo da instalação da máquina local quanto às libs do Python. Dessa forma, o pipenv foi a ferramenta escolhida para manter e gerenciar esse ambiente virtual. Certifique-se de ter o pipenv instalado na sua máquina, o processo é bem simples, portanto iremos pular essa parte aqui no passo-a-passo.

Com o pipenv instalado, vamos criar o nosso ambiente virtual:

```batch
pipenv --python 3.7
```

Ao criar o ambiente, será gerado um arquivo Pipfile que, por ora, só diz que o projeto utiliza o Python na versão 3.7. Esse arquivo será responsável por gerenciar todas as dependências do nosso ambiente virtual. Se você vem do mundo Java, esse arquivo funciona como um pom.xml do maven.

Agora que temos um ambiente virtual par ao nosso projeto, vamos instalar o Django nesse ambiente.

### 2. Instalando Django

Usando o pipenv, utilizaremos o comando abaixo para instalar o Django:

```batch
pipenv install django==3.0
```

Legal, agora nosso ambiente possui o Python e Django, você pode checar isso no Pipfile.

Percebeu que surgiu um novo arquivo aí chamado Pipfile.lock? Esse arquivo é muito importante porque ele é gerado especificando exatamente quais as versões de bibliotecas externas que foram instaladas em sua máquina.

E porque isso é importante? É importante porque caso você precise mudar de máquina enquanto está desenvolvendo sua aplicação, esse arquivo ajudará a replicar o ambiente virtual idêntico em uma nova instalação e com isso você sempre tem a tranquilidade de saber que está usando as mesmas versões e que a compatibilidade entre elas permanece.

### 3. Ativando o ambiente virtual

O ambiente virtual agora existe e já tem a carinha do projeto, mas para o usarmos de fato, precisamos ativá-lo:

```batch
pipenv shell
```

Nosso ambiente agora está ativo, podemos checar usando os comandos:

```batch
pipenv --venv
```

Ou

```batch
pipenv --where
```

Ambos devem apontar ou referenciar o nome do diretório em que criamos o projeto.

### 4. Iniciando um projeto django

O comando abaixo irá criar um diretório config de uma aplicação Django. O "." passado no final do comando é para dizer ao django criar o projeto a partir do diretório raiz. Por padrão, ele criaria um diretório extra e dentro desse diretório criaria o config, mas aqui vai do gosto do freguês e de como se quer organizar o projeto.

```batch
django-admin startproject config .
```

Com o comando executado, nosso projeto ficará com a seguinte estrutura:

```batch
(template_django_with_docker) ➜ :~$ tree
.
├── LICENSE
├── Pipfile
├── Pipfile.lock
├── README.md
├── config
│   ├── __init__.py
│   ├── asgi.py
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
└── manage.py
```
