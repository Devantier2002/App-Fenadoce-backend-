# API de Gestão de Candidatas, Clientes e Votos

Este projeto é uma API desenvolvida com **Express.js** e **Prisma ORM**, focada na gestão de candidatas, clientes e votos. A API permite realizar operações CRUD (Criar, Ler, Atualizar e Deletar) para as entidades **Candidata**, **Cliente** e **Voto**, com validação de dados usando **Zod**.

## Funcionalidades

### 1. **Gestão de Candidatas**
- **GET /candidatas**: Recupera todas as candidatas cadastradas.
- **POST /candidatas**: Cria uma nova candidata, com validação de dados (nome, clube, idade, e sonho).
- **PUT /candidatas/:id**: Atualiza os dados de uma candidata existente.
- **DELETE /candidatas/:id**: Exclui uma candidata.

**Validações para a Candidata**:
- Nome deve ter pelo menos 10 caracteres.
- Idade deve ser maior ou igual a 16 anos.

### 2. **Gestão de Clientes**
- **GET /clientes**: Recupera todos os clientes cadastrados, incluindo os votos associados.
- **POST /clientes**: Cria um novo cliente com validação de dados (nome, email, cidade, e data de nascimento).
- **PUT /clientes/:id**: Atualiza os dados de um cliente existente.
- **DELETE /clientes/:id**: Exclui um cliente.

**Validações para o Cliente**:
- Nome deve ter pelo menos 10 caracteres.
- E-mail deve ter pelo menos 10 caracteres.
- Data de nascimento deve ser válida e no formato `YYYY-MM-DD`.

### 3. **Gestão de Votos**
- **GET /votos**: Recupera todos os votos, incluindo as candidatas e clientes associados.
- **POST /votos**: Cria um novo voto, associando um cliente a uma candidata e, opcionalmente, uma justificativa.
- **DELETE /votos/:id**: Exclui um voto, atualizando a quantidade de votos da candidata.

## Requisitos

- **Node.js** versão 14 ou superior.
- **Prisma Client** para interagir com o banco de dados.
- **Zod** para validação de dados.
- **Express.js** para criação da API.


