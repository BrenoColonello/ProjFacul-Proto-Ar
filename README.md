# Proto-Ar

Proto-Ar é um projeto de exemplo que utiliza Node.js, Express e PostgreSQL para criar uma aplicação web com funcionalidades de login, exibição de dados e gráficos interativos.

## Estrutura do Projeto

Proto-Ar-main/ ├── banco.js ├── compose.yaml ├── package.json ├── package-lock.json ├── server.js ├── public/ │ ├── client.js │ ├── home.html │ ├── site.html │ ├── site.js │ ├── images/ │ │ ├── Dashboard Login.jpg │ │ ├── recarregar.png │ │ └── user.svg │ └── styles/ │ ├── home.css │ └── site.css


## Funcionalidades

- **Backend**:
  - Configuração de um servidor Express ([server.js](server.js)).
  - Conexão com banco de dados PostgreSQL utilizando a biblioteca `postgres` ([banco.js](banco.js)).
  - Criação e manipulação de tabelas no banco de dados.
  - Endpoints para inserção e recuperação de dados.

- **Frontend**:
  - Página de login ([site.html](public/site.html)) com validação simples.
  - Página inicial ([home.html](public/home.html)) que exibe dados em uma tabela e gráficos interativos.
  - Estilização com CSS ([home.css](public/styles/home.css), [site.css](public/styles/site.css)).
  - Gráficos gerados com Chart.js.

- **Banco de Dados**:
  - Tabelas:
    - `lote`: Armazena informações sobre lotes.
    - `dispositivos`: Relaciona dispositivos a lotes.
    - `eventos`: Registra eventos associados a dispositivos.
  - Scripts para criação, inserção e limpeza de dados.

## Pré-requisitos

- Node.js (versão 12 ou superior).
- Docker (para executar o PostgreSQL e o pgAdmin via Docker Compose).

## Instalação

1. Clone o repositório:
   ```bash
   git clone https://github.com/seu-usuario/Proto-Ar.git
   cd Proto-Ar

Instale as dependências:

npm install

Configure o banco de dados:

docker-compose up -d

Certifique-se de que o Docker está instalado e em execução.
Suba os serviços do PostgreSQL e pgAdmin:
Configure o banco de dados no arquivo banco.js (se necessário).

Uso
Inicie o servidor:

node server.js

Acesse a aplicação no navegador:

http://localhost:3000

Faça login com<vscode_annotation details='%5B%7B%22title%22%3A%22hardcoded-credentials%22%2C%22description%22%3A%22Embedding%20credentials%20in%20source%20code%20risks%20unauthorized%20access%22%7D%5D'> as</vscode_annotation> credenciais:

Usuário: admin
Senha: 1234
Explore a página inicial para visualizar os dados e gráficos.

Endpoints
GET /api/data: Retorna todos os dados do banco.
POST /api/insert: Insere um novo evento no banco.
Tecnologias Utilizadas
Backend: Node.js, Express, PostgreSQL.
Frontend: HTML, CSS, JavaScript, Chart.js.
Banco de Dados: PostgreSQL.
Gerenciamento de Dependências: npm.
Containerização: Docker, Docker Compose.
