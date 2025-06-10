# 🛍️ **StoreManager – Sistema de Gerenciamento de Loja**

> **Plataforma acadêmica colaborativa** que centraliza o controle de produtos, clientes, vendas, estoque e finanças para pequenos e médios comércios.

---

## 📚 Sobre o Projeto

O **StoreManager** nasceu da iniciativa de transformar a turma de **Análise e Desenvolvimento de Sistemas (ADS)** em uma **simulação realista de uma empresa de tecnologia colaborativa**. Assim como o projeto‑modelo **Geniws** (Marketplace de Freelancers), nosso objetivo é unir forças para construir um sistema completo que sirva como **laboratório de aprendizado, networking e portfólio profissional**.

* **Aplicação prática** de Front‑end, Back‑end, banco de dados e metodologias ágeis.
* **Participação aberta e voluntária**, respeitando o ritmo de cada integrante.
* **Evolução contínua**: do MVP ao produto utilizável por lojistas reais.

Este projeto é mais do que uma atividade de sala de aula — é uma oportunidade de **construir carreira colaborativamente**.

---

## 🚨 Documentos Obrigatórios (para o time)

| Documento                | Caminho                |
| ------------------------ | ---------------------- |
| **Regras Internas**      | `docs/rules.md`        |
| **Objetivos Detalhados** | `docs/objetivos.md`    |
| **Requisitos**           | `docs/requirements.md` |
| **Visão do Produto**     | `docs/visao.md`        |

> **Leia estes arquivos antes de começar a contribuir.**

---

## 🛠️ Stack Tecnológica

| Camada              | Tecnologias                                                    |
| ------------------- | -------------------------------------------------------------- |
| **Front‑end**       | HTML5 • CSS3 • JavaScript (Vanilla) • *React (opcional)*       |
| **Back‑end Node**   | Node.js • Express.js                                           |
| **Back‑end Java**   | Java • Spring Boot (microservice de produtos & clientes)       |
| **Banco de Dados**  | MySQL (PlanetScale / Neon)                                     |
| **DevOps & Extras** | API REST • GitHub Actions • Chart.js • Axios • bcrypt • dotenv |

---

## 🧩 Funcionalidades Principais (Escopo MVP)

| Módulo               | Descrição                                                                  |
| -------------------- | -------------------------------------------------------------------------- |
| 🔑 **Autenticação**  | Login/cadastro de administradores (bcrypt + JWT)                           |
| 📦 **Produtos**      | CRUD, controle de estoque, fotos e categorias                              |
| 👥 **Clientes**      | Cadastro, histórico de compras                                             |
| 🛒 **Vendas**        | PDV com carrinho, seleção de cliente/produtos, recibo                      |
| 📊 **Estoque**       | Alertas automáticos, movimentações de entrada/saída                        |
| 📈 **Relatórios**    | Gráficos dinâmicos (Chart.js): vendas, produtos mais vendidos, faturamento |
| 💰 **Financeiro**    | Entradas, saídas, despesas, lucro líquido (fase avançada)                  |
| 🖥️ **Painel Admin** | Dashboard com KPIs, metas e alertas                                        |

---

## 🗄️ Estrutura de Banco de Dados (MySQL)

Scripts SQL em `database/schema.sql`. Tabelas‑chave: `usuarios`, `clientes`, `produtos`, `vendas`, `itens_venda`, `estoque_log`, `transacoes`.

---

## 📂 Organização de Repositório

```
storemanager/
├── backend-node/      # API Node.js (auth, vendas, financeiro)
├── backend-java/      # API Java Spring (produtos, clientes, estoque)
├── frontend/          # HTML/CSS/JS ou React
├── docs/              # documentação (rules, objetivos, requisitos…)
├── database/          # scripts SQL e migrations
└── README.md          # (este arquivo)
```

---

## 📅 Status do Projeto

| Fase          | Nome                                      | Status |
| ------------- | ----------------------------------------- | ------ |
| 🧪 **Fase 1** | Onboarding & Preparação                   | ⏳      |
| 🧠 **Fase 2** | Levantamento de Requisitos & Planejamento | ⏳      |
| 🚧 **Fase 3** | MVP – Versão Beta Inicial                 | ⏳      |
| 📝 **Fase 4** | Testes & Validações                       | ⏳      |

---

## 👥 Equipes

* **UX/UI** – prototipação de telas
* **Front‑end** – interface web (HTML/CSS/JS/React)
* **Back‑end Node** – autenticação, vendas, relatórios
* **Back‑end Java** – produtos, clientes, estoque
* **Banco de Dados** – modelagem e scripts SQL
* **QA/DevOps** – testes, CI/CD, qualidade de código

A equipe completa conta com **6 membros** com formações complementares (Java, Node.js, React, HTML/CSS/JS, SQL). As atribuições detalhadas estão em `docs/roles.md`.

---

## 🌐 Extras Planejados (Pós‑MVP)

* Exportação de relatórios em PDF/Excel
* Suporte multiusuário (vendedores)
* Backup automático do banco de dados
* Aplicativo desktop Java FX para operação offline

---

## 💬 Como Contribuir

1. Leia os documentos obrigatórios listados acima.
2. Faça **fork** → crie uma branch com nome descritivo → **Pull Request**.
3. Siga o padrão **Conventional Commits**.
4. Descreva seu PR e vincule‑o a issues.

---

**Happy coding & learning! 🚀**
