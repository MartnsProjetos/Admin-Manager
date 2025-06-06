## Protótipo do `setup.md`

1. **Introdução**: Breve descrição do propósito (configurar o ambiente para desenvolver o Geniws).

2. **Pré-requisitos**:

   - Node.js (v18+)
   - PostgreSQL (v14+)
   - Git
   - Conta no GitHub

3. **Passos de Configuração**:

   - **Clonar repositório**: `git clone https://github.com/seu-repositorio/geniws.git`
   - **Instalar dependências**:
     - Front-end: `cd frontend && npm install`
     - Back-end: `cd backend && npm install`
   - **Configurar banco de dados**:
     - Criar banco: `createdb geniws`
     - Configurar `.env` no back-end:
       ```env
       DATABASE_URL=postgresql://user:password@localhost:5432/geniws
       JWT_SECRET=sua-chave-secreta
       ```
     - Rodar migrações: `cd backend && npm run migrate`
   - **Rodar o projeto**:
     - Front-end: `cd frontend && npm start`
     - Back-end: `cd backend && npm run dev`

4. **Notas**:

   - Verificar portas (ex.: 3000 para front-end, 5000 para back-end).
   - Solução de erros comuns (ex.: `psql: command not found`).

5. **Instalar dependências**:
   - Front-end: `cd frontend && npm install`
   - Back-end: `cd backend && npm install`
6. **Configurar banco de dados**:
   - Criar banco: `createdb geniws`
   - Configurar `backend/.env`:
     ```env
     DATABASE_URL=postgresql://user:password@localhost:5432/geniws
     JWT_SECRET=sua-chave-secreta
     ```
   - Rodar migrações: `cd backend && npm run migrate`
7. **Rodar o projeto**:
   - Front-end: `cd frontend && npm start`
   - Back-end: `cd backend && npm run dev`

## Notas

- Front-end roda na porta 3000, back-end na 5000.
- Se `psql` não for encontrado, instale o PostgreSQL CLI.

```

```

```

```
