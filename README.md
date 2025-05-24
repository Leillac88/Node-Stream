# 👥 Simple User Management API

Este repositório contém uma API REST básica desenvolvida em Node.js usando o módulo `http` nativo. Ela permite gerenciar uma lista de usuários com funcionalidade de criação e listagem. Os dados são armazenados em memória e não são persistentes.

## Funcionalidades

-   **Listar Usuários (GET /users)**: Retorna todos os usuários atualmente armazenados no servidor.
-   **Criar Usuário (POST /users)**: Adiciona um novo usuário à lista. Cada usuário recebe uma **ID única e sequencial** automaticamente e pode incluir **nome, email e endereço**.

## Como Executar o Projeto

1.  **Clone este repositório:**
    ```bash
    git clone [https://github.com/SEU_USUARIO/SEU_REPOSITORIO.git](https://github.com/SEU_USUARIO/SEU_REPOSITORIO.git)
    ```
    (Substitua `SEU_USUARIO/SEU_REPOSITORIO` pelo seu nome de usuário e nome do repositório no GitHub).

2.  **Navegue até a pasta do projeto:**
    ```bash
    cd SEU_REPOSITORIO
    ```

3.  **Inicie o servidor:**
    ```bash
    node server.js
    ```
    O servidor estará rodando em `http://localhost:3333`.

## Endpoints da API

### `GET /users`

-   **Descrição:** Retorna uma lista de todos os usuários.
-   **Método:** `GET`
-   **Exemplo de Resposta:**
    ```json
    [
        {
            "id": 1,
            "name": "Leilla Carvalho",
            "email": "leilla@example.com",
            "address": "Rua Exemplo, 123"
        },
        {
            "id": 2,
            "name": "Outro Usuário",
            "email": "outro@example.com",
            "address": "Avenida Teste, 456"
        }
    ]
    ```

### `POST /users`

-   **Descrição:** Cria um novo usuário.
-   **Método:** `POST`
-   **Corpo da Requisição (JSON):**
    ```json
    {
        "name": "Nome do Usuário",
        "email": "email@example.com",
        "address": "Endereço do Usuário"
    }
    ```
-   **Exemplo de Resposta (sucesso):**
    ```
    Status: 201 Created (sem corpo de resposta padrão, mas o usuário é adicionado)
    ```

## Observações

-   Os dados dos usuários são armazenados **apenas em memória** e serão perdidos ao reiniciar o servidor.
-   Este projeto é um exemplo básico e não inclui validações robustas de entrada, tratamento de erros avançado ou persistência de dados em banco de dados.

---
