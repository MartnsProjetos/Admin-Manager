**# Backend**

Este diretório contém o código da API do Geniws, construída utilizando Node.js e o framework Express.js. Sua estrutura é organizada nos seguintes módulos principais:

- `controllers/`: Responsável por conter a lógica de negócio que manipula as requisições e respostas dos diferentes endpoints da API. Aqui residem as funções que processam os dados e interagem com os modelos.
- `models/`: Define a estrutura dos dados da aplicação. Neste diretório, você encontrará as definições dos modelos de dados, como os esquemas utilizados pelo PostgreSQL para representar as entidades do banco de dados.
- `routes/`: Contém a definição de todas as rotas da API REST. Cada arquivo dentro desta pasta especifica os endpoints disponíveis (URLs), os métodos HTTP suportados (GET, POST, PUT, DELETE, etc.) e os controllers associados para o tratamento das requisições.
- `server.js`: É o ponto de entrada principal da aplicação Node.js. Este arquivo geralmente configura e inicia o servidor Express.js, além de realizar outras configurações essenciais para o funcionamento da API.

Esta organização modular facilita a manutenção, escalabilidade e o entendimento da arquitetura do back-end do Geniws.
