# Pulse API

API RESTful para gerenciamento de loja de eletrônicos, desenvolvida em Node.js, TypeScript, Express e Prisma ORM.

## Funcionalidades
- Cadastro, edição, exclusão e autenticação de clientes
- Cadastro, edição, exclusão e autenticação de administradores
- Cadastro e gerenciamento de produtos, marcas e imagens
- Comentários e respostas de clientes
- Recuperação de senha por e-mail

## Tecnologias Utilizadas
- Node.js
- TypeScript
- Express
- Prisma ORM
- PostgreSQL (NeonDB)
- Zod (validação)
- Nodemailer (e-mail)

## Como rodar localmente

1. **Clone o repositório:**
   ```bash
   git clone <url-do-repo>
   cd pasta-do-projeto
   ```
2. **Instale as dependências:**
   ```bash
   npm install
   ```
3. **Configure o arquivo `.env`:**
   ```env
   DATABASE_URL="<sua-string-de-conexao-postgres>"
   JWT_KEY="<sua-chave-secreta>"
   ```
4. **Rode as migrations e gere o Prisma Client:**
   ```bash
   npx prisma migrate deploy
   npx prisma generate
   ```
5. **Inicie a API:**
   ```bash
   npm run dev
   ```

## Deploy na Vercel
- Configure as variáveis de ambiente `DATABASE_URL` e `JWT_KEY` no painel da Vercel.
- Build Command: `npm run build`
- Output Directory: `dist`

## Endpoints principais
- `/clientes` - CRUD de clientes
- `/admins` - CRUD de administradores
- `/produtos` - CRUD de produtos
- `/marcas` - CRUD de marcas
- `/comentarios` - CRUD de comentários
- `/imagens` - Upload de imagens
- `/dashboard` - Dados para dashboard

## Observações
- O projeto utiliza Prisma com PostgreSQL serverless (NeonDB).
- O deploy é compatível com Vercel Functions.
- Para dúvidas, consulte o código ou abra uma issue.
