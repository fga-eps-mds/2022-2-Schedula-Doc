# Deploy - Schedula - Front

## 1. Histórico de versão

| Versão | Data       | Descrição            | Autor        |
| ------ | ---------- | -------------------- | ------------ |
| 1.0    | 26/01/2023 | Criação do documento | Paulo Victor |
| 2.0    | 30/01/2023 | Adição de passo a passo para deploy com Docker | Paulo Victor |

## Introdução

Neste guia, iremos fornecer uma passo a passo para a geração da build do projeto Schedula(WEB) e as variáveis ambiente necessárias para a execução do mesmo.

---

# Deploy com Docker

## Pré-requisitos
- Docker

## Passo a Passo
O primeiro passo é clonarmos o projeto na máquina. Para isso, utilize o comando abaixo:

```sh
  > git clone https://github.com/fga-eps-mds/2022-2-schedula-front.git
```
---

Para que o projeto funcione conforme o esperado, se faz necessário a adição de variáveis ambientes. Crie um arquivo `.env` na raiz do projeto e adicione  as seguintes variáveis ambiente que são necessárias para o projeto:

```sh
  VITE_PUBLIC_DETALHADOR_CHAMADOS_URL=            # Ex: VITE_PUBLIC_DETALHADOR_CHAMADOS_URL=https://schedula-core.herokuapp.com

  VITE_PUBLIC_GESTOR_DE_USUARIOS_URL=             # Ex: VITE_PUBLIC_GESTOR_DE_USUARIOS_URL=https://schedula-user.herokuapp.com

  VITE_PUBLIC_GERENCIADOR_DE_LOCALIDADES_URL=     # Ex: VITE_PUBLIC_GERENCIADOR_DE_LOCALIDADES_URL=https://schedula-location.herokuapp.com
```

Onde VITE_PUBLIC_DETALHADOR_CHAMADOS_URL é a URL de deploy do serviço de chamados, VITE_PUBLIC_GESTOR_DE_USUARIOS_URL é a URL de deploy do serviço de usuários e VITE_PUBLIC_GERENCIADOR_DE_LOCALIDADES_URL é a URL de deploy do serviço de localidades.

---

Com o clone do repositório concluído, vamos executar o seguinte comando para que o Docker construa o container do projeto.
```sh
  > docker build -t schedula:production . 
```

---

Com a imagem construída com sucesso, podemos passar para a execução desse container.

```sh
  > docker run -it -p 3000:3000 --rm schedula:production
```

### Pronto! Basta acessar o localhost da maquina que a aplicação estará em execução.

---
# Deploy sem docker

## Pré-requisitos

- Node(versão 16 ou maior)
- npm
- Git

---

## Passo a Passo

> O primeiro passo então é instalarmos o NodeJS versão 16(LTS) ou maior na máquina onde será realizado o deploy.

> Caso esteja utilizando alguma solução de deploy de projetos React, muito provavelmente não será necessário realizar nenhuma dos passos desse guia, bastando apenas adicionar as variáveis ambientes descritas no final do guia.

Para instalar o Node, acesse o site oficial da ferramenta e siga o guia de instalação correspondente ao sistema da máquina que será usada no deploy: [Site do NodeJS](https://nodejs.org/pt-br/)

Com o Node e o NPM instalados, podemos seguir com a instalação do Yarn. Para isso, podemos usar o seguinte comando de instalação:

```js
npm install -g yarn
```

Com o Yarn instalado na máquina, precisamos agora clonar o repositório da aplicação. Para isso, utilize o comando abaixo:

```sh
  git clone https://github.com/fga-eps-mds/2022-2-schedula-front.git
```

Após o clone do repositório tiver sido concluído, usaremos os seguintes comandos para gerar o build da aplicação:

```sh
  cd 2022-2-schedula-front # Acessa a pasta da aplicação

  yarn # Irá instalar todas as dependências do projeto

  yarn build # Fará o build do código fonte
```

Feito os passos acima, teremos uma nova pasta criada chamada **dist**. Dentro dessa página teremos todos os arquivos necessários para a hospedagem do projeto em um servidor de páginas estáticas.

> Caso esteja realizando esse processo em sua máquina local e queira ter uma demonstração de como a aplicação está funcionando, basta utilizar o comando `yarn preview` para que a aplicação seja executada usando o código gerado após a build do projeto.

## Variáveis Ambiente

Para que o projeto funcione conforme o esperado, se faz necessário a adição de variáveis ambientes. Caso esteja fazendo isso localmente, crie um arquivo `.env` na raiz do projeto. Caso esteja usando alguma plataforma online, adicione as variáveis conforme orientado pela mesma.

As variáveis necessárias para o projeto são as seguintes:

```sh
  VITE_PUBLIC_DETALHADOR_CHAMADOS_URL=https://schedula-core.herokuapp.com

  VITE_PUBLIC_GESTOR_DE_USUARIOS_URL=https://schedula-user.herokuapp.com

  VITE_PUBLIC_GERENCIADOR_DE_LOCALIDADES_URL=https://schedula-location.herokuapp.com
```

Onde VITE_PUBLIC_DETALHADOR_CHAMADOS_URL é a URL de deploy do serviço de chamados, VITE_PUBLIC_GESTOR_DE_USUARIOS_URL é a URL de deploy do serviço de usuários e VITE_PUBLIC_GERENCIADOR_DE_LOCALIDADES_URL é a URL de deploy do serviço de localidades.

---

## Executando build
 Com o processo da build concluído, o próximo passo é iniciarmos o servidor que irá servir os arquivos estáticos. Para isso, basta executarmos:
 ```sh
  > yarn start
 ```

---

## Resumo (Sem Docker)

```sh
  # Passo 1
  > npm install -g yarn

  # Passo 2
  > git clone https://github.com/fga-eps-mds/2022-2-schedula-front.git

  # Passo 3
  > cd 2022-2-schedula-front

  # Passo 4
  > yarn

  # Passo 5
  > yarn build

  # Passo 6
  Adição das variáveis de ambiente:
  - VITE_PUBLIC_DETALHADOR_CHAMADOS_URL
  - VITE_PUBLIC_GESTOR_DE_USUARIOS_URL
  - VITE_PUBLIC_GERENCIADOR_DE_LOCALIDADES_URL
  
  # Passo 7
  > yarn start

```
