🛍️ Sistema de Gerenciamento de Loja Completo
🎯 Objetivo
Desenvolver uma plataforma completa para que o dono da loja possa gerenciar de forma eficiente:

Produtos

Clientes

Vendas

Estoque

Relatórios

Login/Admin

🛠️ Tecnologias Utilizadas
Camada	Tecnologia
Frontend	HTML5, CSS3, JavaScript (Vanilla)
Backend	Node.js com Express.js
Banco de Dados	MySQL (exemplo: Neon, PlanetScale)
Desktop (Opcional)	Java (ex: painel local)

Bibliotecas e Ferramentas Extras
Chart.js (gráficos no dashboard)

bcrypt (criptografia de senhas)

dotenv (variáveis de ambiente)

Axios / Fetch (comunicação frontend-backend)

🧱 Funcionalidades Principais
Módulo	Funcionalidade
Autenticação	Login e cadastro de administradores
Produtos	Cadastro, edição, exclusão, consulta e controle de estoque
Clientes	Cadastro de clientes e histórico de compras
Vendas	Registrar vendas, selecionar clientes e produtos, gerar recibo
Estoque	Alertas de estoque baixo, entrada e saída de produtos
Relatórios	Relatórios de vendas, produtos mais vendidos e faturamento
Financeiro	Controle de entradas, saídas, despesas e lucro líquido
Painel Admin	Visão geral com gráficos, alertas e metas

🧩 Estrutura do Banco de Dados (MySQL)
sql
Copiar
Editar
CREATE TABLE usuarios (
  id INT AUTO_INCREMENT PRIMARY KEY,
  nome VARCHAR(100),
  email VARCHAR(100) UNIQUE,
  senha_hash VARCHAR(255)
);

CREATE TABLE clientes (
  id INT AUTO_INCREMENT PRIMARY KEY,
  nome VARCHAR(100),
  email VARCHAR(100),
  telefone VARCHAR(20),
  endereco TEXT
);

CREATE TABLE produtos (
  id INT AUTO_INCREMENT PRIMARY KEY,
  nome VARCHAR(100),
  descricao TEXT,
  preco DECIMAL(10,2),
  estoque INT
);

CREATE TABLE vendas (
  id INT AUTO_INCREMENT PRIMARY KEY,
  id_cliente INT,
  data DATETIME,
  total DECIMAL(10,2),
  FOREIGN KEY (id_cliente) REFERENCES clientes(id)
);

CREATE TABLE itens_venda (
  id INT AUTO_INCREMENT PRIMARY KEY,
  id_venda INT,
  id_produto INT,
  quantidade INT,
  subtotal DECIMAL(10,2),
  FOREIGN KEY (id_venda) REFERENCES vendas(id),
  FOREIGN KEY (id_produto) REFERENCES produtos(id)
);

CREATE TABLE estoque_log (
  id INT AUTO_INCREMENT PRIMARY KEY,
  id_produto INT,
  tipo ENUM('entrada','saida'),
  quantidade INT,
  data DATETIME,
  FOREIGN KEY (id_produto) REFERENCES produtos(id)
);

CREATE TABLE transacoes (
  id INT AUTO_INCREMENT PRIMARY KEY,
  tipo ENUM('entrada','saida'),
  descricao TEXT,
  valor DECIMAL(10,2),
  data DATETIME
);
📱 Telas do Sistema
Tela de Login e Cadastro

Dashboard Geral (resumo: vendas, estoque, produtos)

Cadastro e Listagem de Produtos

Cadastro e Listagem de Clientes

Tela de Nova Venda com carrinho

Controle de Estoque com alertas

Relatórios em gráficos (Chart.js)

Tela Financeira (lucro, entradas e saídas)

👥 Divisão de Tarefas (Exemplo para Equipe)
Membro	Responsável por
Frontend 1	Telas HTML/CSS de produtos, clientes e vendas
Frontend 2	Dashboard, gráficos, responsividade
Backend 1	Rotas e APIs para produtos, clientes e vendas
Backend 2	Autenticação, login, sistema financeiro
Banco de Dados	Modelagem, criação e manutenção do banco
Java (Opcional)	Versão desktop local do sistema

🌐 Funcionalidades Extras (Opcional)
Exportar relatórios em PDF ou Excel

Gerar recibo de venda automaticamente

Sistema multiusuário (funcionários com diferentes permissões)

Backup automático do banco de dados

Responsividade para celulares e tablets
