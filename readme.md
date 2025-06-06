# 🛍️ Sistema de Gerenciamento de Loja Completo

---

## 🎯 Objetivo do Projeto

Construir uma plataforma completa para que o dono da loja possa gerenciar:

- 📦 Produtos  
- 👥 Clientes  
- 🛒 Vendas  
- 📊 Estoque  
- 📈 Relatórios  
- 🔐 Login/Admin  

---

## 🛠️ Tecnologias Utilizadas

| Camada            | Tecnologia                        |
|-------------------|---------------------------------|
| **Frontend**      | HTML5, CSS3, JavaScript (Vanilla) |
| **Backend**       | Node.js, Express.js              |
| **Banco de Dados**| MySQL (ex: Neon, PlanetScale)   |
| **Desktop (Opcional)** | Java (painel para controle local) |

### 📚 Bibliotecas e Ferramentas Extras

- Chart.js – gráficos dinâmicos no dashboard  
- bcrypt – criptografia de senhas  
- dotenv – variáveis de ambiente seguras  
- Axios / Fetch – comunicação frontend-backend via API  

---

## 🧩 Funcionalidades Principais

| Módulo          | Funcionalidade                                         |
|-----------------|-------------------------------------------------------|
| 🔑 Autenticação | Login e cadastro de administradores                    |
| 📦 Produtos     | Cadastro, edição, exclusão, consulta, controle de estoque |
| 👥 Clientes     | Cadastro e histórico de compras                         |
| 🛒 Vendas       | Registrar vendas, selecionar clientes/produtos, gerar recibos |
| 📊 Estoque      | Alertas para estoque baixo, movimentação de produtos    |
| 📈 Relatórios   | Relatórios de vendas, produtos mais vendidos, faturamento |
| 💰 Financeiro   | Controle de entradas, saídas, despesas e lucro líquido  |
| 🖥️ Painel Admin| Visão geral com gráficos, alertas e metas               |

---

## 🗄️ Estrutura do Banco de Dados (MySQL)

```sql
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
```


📱 Telas do Sistema
🔐 Tela de Login e Cadastro

📊 Dashboard Geral com cards de resumo (vendas, estoque, produtos)

📦 Cadastro e listagem de produtos

👥 Cadastro e listagem de clientes

🛒 Tela de nova venda com carrinho

📦 Controle de estoque com alertas

📈 Relatórios em gráficos interativos (Chart.js)

💰 Tela de finanças (lucro, entradas e saídas)

👥 Divisão de Tarefas (Exemplo para Equipe)
Membro	Responsável por...
Frontend 1	Telas HTML/CSS de produtos, clientes e vendas
Frontend 2	Dashboard, gráficos e responsividade
Backend 1	Rotas Node.js para produtos, clientes e vendas
Backend 2	Login, autenticação, sistema financeiro
Banco de Dados	Modelagem e criação do banco e relacionamentos
Java (Opcional)	Versão desktop simples para controle local

🌐 Extras (Opcional)
Exportar relatórios em PDF ou Excel

Gerar recibo de venda

Sistema multiusuário (mais de um funcionário)

Backup automático do banco de dados

Layout responsivo para celular e tablet

Se quiser, posso ajudar a montar:

Estrutura de pastas do projeto

Modelo do banco de dados MySQL completo

Roteiro passo a passo para desenvolvimento em grupo

Protótipos de telas
