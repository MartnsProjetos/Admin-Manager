## Protótipo `api.md`

1. **Introdução:** Breve descrição da API REST do Geniws (ex.: suporta funcionalidades do MVP como cadastro, projetos, propostas).

2. **Configuração:**

   - Base URL (ex.: https://api.geniws.com).
   - Autenticação (ex.: JWT via header Authorization: Bearer <token>).

3. **Endpoints (para cada um, inclua):**

   - Método e URL (ex.: GET /api/users).
   - Descrição: Função do endpoint (ex.: Lista usuários).
   - Parâmetros: Query/body, se aplicável (ex.: { "skills": "React" }).
   - Resposta de Sucesso: Código HTTP (ex.: 200), exemplo JSON (ex.: { "users": [{ "id": 1, "name": "João" }] }).
   - Erros: Códigos HTTP (ex.: 400, 401), exemplo JSON (ex.: { "error": "Email inválido" }).

4. **Exemplos de Requisições:**

   - Exemplo com curl ou Postman (ex.: curl -H "Authorization: Bearer <token>" https://api.geniws.com/api/projects).

5. **Endpoints Principais (baseado em requirements.md):**

   - GET /api/users, POST /api/users
   - GET /api/projects, POST /api/projects
   - GET /api/proposals, POST /api/proposals
   - GET /api/ratings, POST /api/ratings
   - GET /api/messages, POST /api/messages
   - POST /api/auth/register, POST /api/auth/login

6. **Notas:**
   - Formato JSON, HTTPS obrigatório, limites de taxa (se aplicável).
