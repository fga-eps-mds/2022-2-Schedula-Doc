# Deploy - Schedula - Back

## 1. Histórico de versão

| Versão | Data       | Descrição            | Autor        |
| ------ | ---------- | -------------------- | ------------ |
| 1.0    | 27/01/2023 | Criação do documento | Mateus Gomes e Vinícius Saturnino |

## 2. Introdução

Neste guia, iremos fornecer uma passo a passo para instalação e deploy dos serviços Back-end do projeto Schedula.

---

## 3. Pré-requisitos

- Docker
- Docker-compose
- Git

---

## 4. Repositórios no GitHub

- Repositório de usuário: https://github.com/fga-eps-mds/2022-2-schedula-gestor-de-usuarios

- Repositório de localidades: https://github.com/fga-eps-mds/2022-2-schedula-gerenciador-de-localidades

- Repositório de chamados: https://github.com/fga-eps-mds/2022-2-schedula-detalhador-de-chamados

---

## 5. Passo a passo

> O primeiro passo é clonar os repositórios.

```shell
$ git clone <repo-link>
```

> Depois, deve-se preencher o arquivo `.env` como está exemplificado no arquivo `.env.example`.


> E por último, deve-se subir o ambiente docker local.

```shell
$ docker compose up --build
```

---

##  6. Deploy

### 6.1 Variáveis de ambiente no GitHub

Para utilizar o pipeline de CD integrado com a plataforma Heroku, deve-se configurar algumas variáveis de ambiente nos repositórios GitHub. Na aba `settings` do repositório clonado, em `Security > Secrets and variables > Actions`, deve-se adicionar as seguintes variáveis.

- HEROKU_EMAIL: email da conta do heroku dona do app de hospedagem para o serviço
- HEROKU_API_KEY: api key da conta heroku no qual o serviço será hospedado
- HEROKU_APP_NAME: nome do app criado no heroku para hospedar o serviço

### 6.2 Variáveis de ambiente de deploy

O serviço de hospedagem deve ter as mesmas variáveis de ambiente especificadas na seção de utilização do ambiente, mas neste caso, com os valores de produção. Estas variáveis são:

- DATABASE_DB: nome do banco de dados
- DATABASE_HOST: host do banco de dados
- DATABASE_PASS: senha do banco de dados
- DATABASE_PORT: porta do banco de dados
- DATABASE_USER: usuário do banco de dados
- ENVIRONMENT: ambiente da execução, o código apenas verifica se esta variável é PRODUCTION, caso seja qualquer outro valor, ele trata como código local de desenvolvimento
- NPM_CONFIG_PRODUCTION: esta é uma variável específica do heroku, que foi necessário dar o valor de _false_ para o heroku conseguir ler a configuração do npm e conseguir rodar o código em nest

---

## 7 Pipelines de CI/CD

Na pasta `.github` na raíz do projeto dentro de `workflows`, estão configurados alguns pipelines orquestrados para desenvolvimento e deploy do repositório.

### 7.1 Workflow de CI

O workflow de CI serve para garantir a cobertura de testes.

### 7.2 Workflow de CD

O workflow de CD serve para fazer o deploy na plataforma do Heroku utilizando as variáveis de produção configuradas anteriormente. Esse pipeline depende do pipeline de CI.