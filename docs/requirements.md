# 📋 Requisitos do Projeto Geniws

Este documento consolida os requisitos funcionais, não funcionais e técnicos do projeto **Geniws**, com base nas funcionalidades descritas em `vision.md` e `objectives.md`. As histórias de usuário detalham as principais funcionalidades da plataforma, com critérios de aceitação para orientar o desenvolvimento.

---

## 🧑‍💻 Histórias de Usuário

### 1. Cadastro de Freelancer

**Como freelancer**, quero criar um perfil detalhado com minhas competências técnicas e portfólio, para que contratantes possam avaliar minha experiência e me encontrar.

**Critérios de Aceitação:**

- O formulário de cadastro deve incluir campos para nome, email, senha, habilidades, experiência, link do GitHub/GitLab e certificações.
- O perfil deve ser salvo no banco de dados e exibido em uma página pública acessível.
- O sistema deve validar que o email é único e está em formato válido.
- Após o cadastro, o freelancer recebe uma confirmação por email.

---

### 2. Cadastro de Contratante

**Como contratante**, quero criar uma conta com informações básicas, para que eu possa publicar projetos e gerenciar propostas.

**Critérios de Aceitação:**

- O formulário de cadastro deve incluir campos para nome, email, senha e tipo de contratante (ex.: empresa, indivíduo).
- A conta deve ser salva no banco de dados e permitir login imediato.
- O sistema deve validar que o email é único.
- Após o cadastro, o contratante é redirecionado para um dashboard inicial.

---

### 3. Publicação de Projetos

**Como contratante**, quero publicar um projeto com detalhes específicos, para que freelancers possam se candidatar.

**Critérios de Aceitação:**

- O formulário de publicação deve incluir título, descrição, tecnologias requeridas, orçamento estimado e prazo.
- O projeto deve ser salvo no banco de dados e listado publicamente após aprovação do contratante.
- O contratante recebe uma notificação (ex.: via dashboard ou email) após a publicação.
- O sistema deve validar que todos os campos obrigatórios estão preenchidos.

---

### 4. Busca de Projetos

**Como freelancer**, quero buscar projetos por tecnologia ou palavra-chave, para que eu encontre oportunidades relevantes para minhas habilidades.

**Critérios de Aceitação:**

- A interface de busca deve oferecer filtros por tecnologia (ex.: JavaScript, Python) e palavra-chave (ex.: "web app").
- Os resultados devem ser exibidos em menos de 2 segundos.
- A lista de projetos deve suportar ordenação por relevância, data de publicação ou orçamento.
- Cada projeto listado deve mostrar título, descrição resumida, tecnologias e orçamento.

---

### 5. Envio de Propostas

**Como freelancer**, quero enviar uma proposta detalhada para um projeto, para que o contratante avalie minha candidatura.

**Critérios de Aceitação:**

- O formulário de proposta deve incluir campos para mensagem personalizada, prazo estimado e valor proposto.
- A proposta deve ser salva no banco de dados e vinculada ao projeto e ao freelancer.
- O contratante recebe uma notificação sobre a nova proposta.
- O freelancer pode visualizar o status da proposta (ex.: enviada, visualizada, aceita).

---

### 6. Avaliação de Freelancers

**Como contratante**, quero avaliar um freelancer após a conclusão de um projeto, para que outros contratantes conheçam sua reputação.

**Critérios de Aceitação:**

- O formulário de avaliação deve incluir uma pontuação (ex.: 1 a 5 estrelas) e um comentário opcional.
- A avaliação deve ser salva no banco de dados e vinculada ao perfil do freelancer.
- A média das avaliações deve ser exibida no perfil público do freelancer.
- O freelancer recebe uma notificação sobre a nova avaliação.

---

### 7. Busca e Seleção de Freelancers

**Como contratante**, quero buscar freelancers por habilidades ou avaliações, para que eu encontre o profissional ideal para meu projeto.

**Critérios de Aceitação:**

- A interface de busca deve oferecer filtros por habilidades (ex.: React, UI/UX) e pontuação mínima de avaliações.
- Os resultados devem ser exibidos em menos de 2 segundos.
- Cada freelancer listado deve mostrar nome, habilidades, link do portfólio e média de avaliações.
- O contratante pode acessar o perfil completo do freelancer a partir dos resultados.

---

### 8. Sistema de Mensagens

**Como contratante ou freelancer**, quero enviar mensagens diretas para negociar projetos, para que possamos discutir detalhes antes da contratação.

**Critérios de Aceitação:**

- A plataforma deve oferecer uma interface de mensagens integrada, acessível a partir do dashboard.
- As mensagens devem ser salvas no banco de dados e vinculadas aos usuários envolvidos.
- O sistema deve notificar o destinatário sobre novas mensagens (ex.: via dashboard ou email).
- Apenas usuários autenticados podem enviar mensagens.

---

### 9. Dashboard de Gerenciamento

**Como contratante**, quero um dashboard para gerenciar meus projetos e propostas, para que eu acompanhe o progresso facilmente.

**Critérios de Aceitação:**

- O dashboard deve exibir uma lista de projetos publicados, com status (ex.: aberto, em andamento, concluído).
- O dashboard deve mostrar propostas recebidas para cada projeto, com opção de aceitar ou rejeitar.
- O dashboard deve ser acessível apenas para contratantes autenticados.
- A interface deve ser responsiva e carregar em menos de 3 segundos.

---

### 10. Verificação de Perfil

**Como freelancer**, quero obter um selo de "Freelancer Verificado", para que meu perfil ganhe mais credibilidade.

**Critérios de Aceitação:**

- O sistema deve oferecer um processo de verificação (ex.: validação comunitária ou comprovação técnica, como certificados).
- O selo deve ser exibido no perfil público do freelancer.
- O processo de verificação deve ser documentado em um guia de boas práticas.
- Apenas freelancers com verificação aprovada recebem o selo.

---

## ⚙️ Requisitos Não Funcionais

- A plataforma deve ser responsiva, funcionando corretamente em dispositivos móveis (mínimo 320px) e desktop (até 1920px).
- A API deve responder a requisições simples (ex.: busca de projetos) em menos de 2 segundos.
- O sistema deve suportar até 1.000 usuários simultâneos na versão beta, com tempo de resposta aceitável.
- A plataforma deve garantir segurança de dados, usando HTTPS e hash de senhas (ex.: bcrypt).
- A interface deve seguir padrões de acessibilidade (ex.: WCAG 2.1, nível AA).

---

## 🧱 Requisitos Técnicos

### 🗄️ Banco de Dados: PostgreSQL

Tabelas:

- **Usuários (`users`)**: id, nome, email, senha, habilidades, link GitHub, certificações.
- **Projetos (`projects`)**: id, título, descrição, tecnologias, orçamento, prazo, contratante_id.
- **Propostas (`proposals`)**: id, projeto_id, freelancer_id, mensagem, prazo, valor.
- **Avaliações (`ratings`)**: id, freelancer_id, contratante_id, pontuação, comentário.
- **Mensagens (`messages`)**: id, remetente_id, destinatário_id, conteúdo, data.

---

### 🔗 API REST: Endpoints principais

- `/api/users`

  - GET: listar
  - POST: cadastrar

- `/api/projects`

  - GET: listar
  - POST: publicar

- `/api/proposals`

  - POST: enviar proposta
  - GET: listar por projeto

- `/api/ratings`

  - POST: avaliar
  - GET: listar por freelancer

- `/api/messages`
  - POST: enviar
  - GET: listar por usuário

---

### 🔐 Autenticação

- JWT para proteger endpoints sensíveis (ex.: `POST /api/projects`)

---

### 🧑‍🎨 Front-end

- React.js com Tailwind CSS para interfaces responsivas

---

### 🧑‍💻 Back-end

- Node.js/Express.js para lógica de negócio e APIs

---

### 🚀 Deploy

- Hospedagem em plataformas como:
  - **Vercel** (front-end)
  - **Render** (back-end)

---

### 🗂️ Versionamento

- Git/GitHub com branches por funcionalidade (ex.: `feature/backend-users`)
