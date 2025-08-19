# 🍽️ API Restaurant

![Node.js](https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-07405E?style=for-the-badge&logo=sqlite&logoColor=white)
![Knex.js](https://img.shields.io/badge/Knex.js-D26B38?style=for-the-badge&logo=knex&logoColor=white)
![Zod](https://img.shields.io/badge/Zod-3E67B1?style=for-the-badge&logoColor=white)

API RESTful desenvolvida em **Node.js (TypeScript)** com **Express**, projetada para gerenciar pedidos, mesas e produtos de um restaurante.  
Este projeto foi construído com foco em boas práticas de arquitetura, validações, tratamento de erros e organização de código.

---

## 📌 Funcionalidades

- Gerenciamento de **produtos**  
- Controle de **mesas** e **sessões de mesas**  
- Registro e acompanhamento de **pedidos**  
- Validação de dados com **Zod**  
- Banco de dados relacional com **SQLite + Knex**  
- Estrutura modular (controllers, routes, middlewares, utils)  

---

## 🛠️ Tecnologias Utilizadas

- [Node.js](https://nodejs.org/) + [TypeScript](https://www.typescriptlang.org/)  
- [Express](https://expressjs.com/)  
- [Knex.js](https://knexjs.org/)  
- [SQLite](https://www.sqlite.org/)  
- [Zod](https://zod.dev/) (validações)  

---

## 📂 Estrutura do Projeto

```
api-restaurant/
 ├── seeds/                 # Scripts para popular o banco
 ├── src/
 │   ├── controllers/       # Lógica dos endpoints
 │   ├── database/
 │   │   ├── migrations/    # Criação das tabelas
 │   │   ├── types/         # Tipagens dos repositórios
 │   │   ├── knex.ts        # Configuração do Knex
 │   ├── middlewares/       # Middlewares globais
 │   ├── routes/            # Rotas da aplicação
 │   ├── utils/             # Classes utilitárias
 │   └── server.ts          # Ponto de entrada
 ├── request_insomnia.yaml  # Coleção do Insomnia para testar
 ├── package.json
 ├── tsconfig.json
 └── knexfile.ts
```

---

## 🚀 Como Rodar o Projeto

### 1️⃣ Clonar o repositório
```bash
git clone https://github.com/LuanMarques-Dev/api-restaurant.git
cd api-restaurant
```

### 2️⃣ Instalar dependências
```bash
npm install
```

### 3️⃣ Rodar as migrations
```bash
npm run knex -- migrate:latest
```

### 4️⃣ Executar os seeds (popular produtos e mesas)
```bash
npm run knex -- seed:run
```

### 5️⃣ Iniciar servidor em modo desenvolvimento
```bash
npm run dev
```

Servidor rodará em:  
👉 `http://localhost:3000`

---

## 📬 Endpoints Principais

### Produtos
- `GET /products` → Lista todos os produtos  
- `POST /products` → Cadastra um novo produto  

### Mesas
- `GET /tables` → Lista mesas disponíveis  
- `POST /tables` → Cria uma nova mesa  

### Sessões de Mesa
- `POST /tables-sessions` → Abre uma sessão para uma mesa  

### Pedidos
- `POST /orders` → Cria um pedido para uma mesa  
- `GET /orders/:id` → Busca detalhes de um pedido  

---

## 🧪 Testando com Insomnia/Postman

Na raiz do projeto existe o arquivo **`request_insomnia.yaml`** com todas as rotas configuradas.  
Basta importar no Insomnia e testar rapidamente.

---

## ⚙️ Scripts Disponíveis

- `npm run dev` → Inicia servidor com hot-reload  
- `npm run knex -- migrate:latest` → Executa migrations  
- `npm run knex -- seed:run` → Executa seeds  

---

## 👨‍💻 Autor

Desenvolvido por **[Luan Marques](https://github.com/LuanMarques-Dev)** 🚀  
Formado em Análise e Desenvolvimento de Sistemas | Estudante de Engenharia de Software | Foco em **Back-end & Full-stack Development**.

---

## 📄 Licença
Projeto licenciado sob a **ISC License**.
