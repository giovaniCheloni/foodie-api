# Documentação da API Foodie

## Descrição
Esta aplicação é uma API para gerenciar entidades relacionadas à alimentação, como categorias, banners, empresas, pedidos e usuários. A API utiliza JWT para autenticação e oferece vários endpoints para operações CRUD.

## Instalação
Para instalar a aplicação, siga os passos abaixo:
1. Clone o repositório:
   ```bash
   git clone https://github.com/seu_usuario/foodie-api.git
   ```
2. Navegue até o diretório do projeto:
   ```bash
   cd foodie-api
   ```
3. Instale as dependências:
   ```bash
   npm install
   ```

## Uso
A API pode ser utilizada através de requisições HTTP. Abaixo estão exemplos de como utilizar os endpoints.

## Endpoints

### Categorias
- **GET /categorias**
  - Retorna uma lista de categorias.

### Banners
- **GET /banners**
  - Retorna uma lista de banners.

### Empresas
- **GET /empresas/destaques**
  - Retorna uma lista de empresas em destaque.
  
- **GET /empresas**
  - Retorna uma lista de todas as empresas.

- **POST /empresas/:id_empresa/favoritos**
  - Adiciona uma empresa aos favoritos do usuário.

- **DELETE /empresas/:id_empresa/favoritos**
  - Remove uma empresa dos favoritos do usuário.

- **GET /empresas/:id_empresa/cardapio**
  - Retorna o cardápio de uma empresa.

- **GET /empresas/:id_empresa/produtos/:id_produto**
  - Retorna detalhes de um produto específico.

### Pedidos
- **GET /pedidos**
  - Retorna uma lista de pedidos.

- **GET /pedidos/:id_pedido**
  - Retorna detalhes de um pedido específico.

- **POST /pedidos**
  - Cria um novo pedido.

### Usuários
- **GET /usuarios/favoritos**
  - Retorna uma lista de favoritos do usuário.

- **POST /usuarios/login**
  - Realiza o login do usuário.

- **POST /usuarios**
  - Cria um novo usuário.

- **GET /usuarios/perfil**
  - Retorna o perfil do usuário.

## Autenticação
A API utiliza JWT para autenticação. Para acessar os endpoints protegidos, inclua o token JWT no cabeçalho da requisição:
```
Authorization: Bearer <seu_token_jwt>
