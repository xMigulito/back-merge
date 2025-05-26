# Backend Merge Towers

Backend para o jogo Merge Towers desenvolvido com Node.js, TypeScript, Express e PostgreSQL.

## Requisitos

- Node.js (versão 14 ou superior)
- PostgreSQL
- npm ou yarn

## Configuração

1. Clone o repositório
2. Instale as dependências:
```bash
npm install
```

3. Configure o arquivo `.env` com suas credenciais do PostgreSQL:
```
DATABASE_URL="postgresql://seu_usuario:sua_senha@localhost:5432/merge_towers?schema=public"
JWT_SECRET="sua_chave_secreta_muito_segura"
```

4. Execute as migrações do banco de dados:
```bash
npm run prisma:migrate
```

5. Gere o cliente Prisma:
```bash
npm run prisma:generate
```

## Executando o projeto

Para desenvolvimento:
```bash
npm run dev
```

Para produção:
```bash
npm run build
npm start
```

## Endpoints

### Criar/Buscar Usuário
- **POST** `/api/users`
- Body: `{ "name": "nome_do_usuario" }`
- Retorna: `{ user: { id, name }, token: "jwt_token" }`

### Teste de Autenticação
- **GET** `/api/test`
- Header: `Authorization: Bearer seu_token_jwt`
- Retorna: `{ userId: id_do_usuario }` 