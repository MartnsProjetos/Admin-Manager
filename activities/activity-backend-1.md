# 🧩 Atividade 4: Desenvolvimento do Back-End com Node.js/Express.js e PostgreSQL

Esta atividade visa capacitar os participantes a construir uma API robusta e um banco de dados estruturado para a plataforma Geniws, garantindo a funcionalidade do back-end e a integração com o front-end.

- 🔰 **Líder da equipe:** [A ser definido]
- 🔗 **GitHub:**

---

## 🎯 Objetivo Geral

Desenvolver a infraestrutura do back-end do MVP da plataforma Geniws, criando uma API REST funcional e um banco de dados relacional que suporte as funcionalidades principais, como cadastro de usuários, gerenciamento de perfis e listagem de projetos.

### ❗ Dor Existente

Muitas plataformas freelancer sofrem com APIs lentas, mal estruturadas ou com problemas de segurança, dificultando a interação com o front-end. Nosso objetivo é criar um back-end confiável, seguro e bem documentado desde o início, que atenda às necessidades do front-end e facilite a escalabilidade futura.

---

## 🎓 Objetivos de Aprendizagem

### 🔗 Desenvolvimento de APIs REST

- Compreender e aplicar os fundamentos de APIs REST (métodos HTTP, endpoints, status codes).
- Desenvolver endpoints com Node.js e Express.js para operações CRUD (Create, Read, Update, Delete).

### 🧱 Modelagem e Gerenciamento de Banco de Dados

- Aprender a projetar esquemas de banco de dados relacionais com PostgreSQL.
- Implementar migrações de banco de dados para criar e gerenciar tabelas.

### 🔐 Segurança e Validação

- Aplicar validação de dados e tratamento de erros para garantir a robustez da API.
- Implementar autenticação básica (ex.: JWT) para proteger endpoints.

### 🤝 Integração e Colaboração

- Trabalhar em conjunto com a equipe de front-end para definir contratos de API (estruturas JSON, endpoints).
- Utilizar Git e GitHub com branches específicas para cada funcionalidade, promovendo um fluxo de trabalho organizado.

---

## 🛠️ Atividades da Equipe de Back-End

O esquadrão de back-end será responsável por construir a API e o banco de dados que suportam as funcionalidades principais da plataforma Geniws, garantindo integração com o front-end.

### 1️⃣ Configuração do Projeto Back-End

- Configurar um projeto Node.js com Express.js
- Instalar dependências necessárias (ex.: `express`, `pg` para PostgreSQL, `dotenv` para variáveis de ambiente)
- Configurar o PostgreSQL localmente ou em um serviço gratuito (ex.: Render, Neon)

### 2️⃣ Modelagem do Banco de Dados

Projetar o esquema do banco de dados para suportar:

- Tabela `users` (id, nome, email, senha, habilidades, link GitHub)
- Tabela `projects` (id, título, descrição, tecnologias, orçamento, prazo, contratante_id)
- Tabela `skills` (id, nome) para habilidades associadas a usuários e projetos

Criar migrações usando uma ferramenta como `knex.js` ou scripts SQL diretos.

### 3️⃣ Desenvolvimento de Endpoints da API

Criar ao menos 4 endpoints REST:

- `GET /api/users`: Listar usuários (com filtros opcionais por habilidades)
- `POST /api/users`: Cadastrar um novo usuário
- `GET /api/projects`: Listar projetos disponíveis
- `POST /api/projects`: Criar um novo projeto

Implementar validação de entrada (ex.: usando `express-validator`) e tratamento de erros.

### 4️⃣ Implementação de Autenticação Básica

- Configurar autenticação com JWT (JSON Web Token) para proteger endpoints sensíveis (ex.: `POST /api/projects`)
- Criar endpoints de autenticação:
  - `POST /api/auth/register`: Registrar um novo usuário
  - `POST /api/auth/login`: Fazer login e retornar um token JWT

### 5️⃣ Documentação da API

- Documentar os endpoints em um arquivo `docs/api.md` ou usando ferramentas como Swagger/Postman
- Incluir exemplos de requisições e respostas (ex.: JSON esperado)

### 6️⃣ Testes Iniciais

- Escrever testes unitários para pelo menos 2 endpoints usando uma ferramenta como Jest ou Mocha
- Testar manualmente os endpoints com Postman para garantir funcionalidade

---

## 🧪 Boas Práticas com Git

- Criar uma branch para cada funcionalidade, com nome padronizado:  
  `feature/backend-nome-da-funcao` (ex.: `feature/backend-user-endpoints`)
- Submeter pull requests (PRs) com descrições claras e solicitar revisões de colegas

---

## 📦 Entregáveis

- ✅ Projeto back-end funcional com Node.js/Express.js e PostgreSQL
- ✅ Banco de dados configurado com tabelas `users`, `projects` e `skills`
- ✅ API REST com pelo menos 4 endpoints implementados (`GET /api/users`, `POST /api/users`, `GET /api/projects`, `POST /api/projects`)
- ✅ Autenticação básica com JWT para endpoints protegidos
- ✅ Documentação da API em `docs/api.md` ou ferramenta equivalente
- ✅ Testes unitários para pelo menos 2 endpoints
- ✅ Código versionado no GitHub com branches nomeadas por funcionalidade (`feature/backend-nome-da-funcao`)
