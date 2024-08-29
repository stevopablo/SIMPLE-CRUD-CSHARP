
# Agenda API
Primeira CRUD COM C# USANDO ENTITY
 API simples para gerenciar uma agenda, construída com ASP.NET Core e Entity Framework Core.

## Começando

### Pré-requisitos

- .NET 6 SDK
- MySQL Server
- Visual Studio ou Visual Studio Code

### Instalação

1. **Clone o repositório:**
    ```bash
    git clone https://github.com/yourusername/agenda-api.git
    cd agenda-api
    ```

2. **Configure o banco de dados:**
    - Certifique-se de que o MySQL Server está em execução.
    - Crie um banco de dados chamado `agenda_db`.
    - Atualize a string de conexão em `appsettings.json`:
      ```json
      "ConnectionStrings": {
        "conexaoPadrao": "Server=localhost;Database=agenda_db;User=root;Password=yourpassword;"
      }
      ```

3. **Execute a aplicação:**
    ```bash
    dotnet run
    ```

### Endpoints

1. **Criar um novo contato**
   - **Método**: `POST`
   - **URL**: `/contato`
   - **Descrição**: Cria um novo contato.
   - **Corpo da Requisição**: Objeto `Contato`
   - **Resposta**: O objeto `Contato` criado

2. **Obter um contato por ID**
   - **Método**: `GET`
   - **URL**: `/contato/{id}`
   - **Descrição**: Recupera um contato pelo seu ID.
   - **Resposta**: O objeto `Contato` com o ID especificado, ou `404 Not Found` se o contato não existir.

3. **Obter contatos por nome**
   - **Método**: `GET`
   - **URL**: `/contato/nome/{nome}`
   - **Descrição**: Recupera contatos cujos nomes contêm a string especificada.
   - **Resposta**: Uma lista de objetos `Contato` que correspondem aos critérios de pesquisa.

4. **Atualizar um contato**
   - **Método**: `PUT`
   - **URL**: `/contato/update/{id}`
   - **Descrição**: Atualiza um contato existente.
   - **Corpo da Requisição**: Objeto `Contato`
   - **Resposta**: O objeto `Contato` atualizado, ou `404 Not Found` se o contato não existir.

5. **Deletar um contato**
   - **Método**: `DELETE`
   - **URL**: `/contato/{id}`
   - **Descrição**: Deleta um contato pelo seu ID.
   - **Resposta**: `204 No Content` se a exclusão for bem-sucedida, ou `404 Not Found` se o contato não existir.

### Tecnologias Utilizadas

- ASP.NET Core
- Entity Framework Core
- MySQL
- Swagger

### Contribuindo

1. Faça um fork do repositório.
2. Crie uma nova branch (`git checkout -b feature-branch`).
3. Faça suas alterações.
4. Commit suas alterações (`git commit -m 'Add some feature'`).
5. Push para a branch (`git push origin feature-branch`).
6. Abra um pull request.

### Licença

Este projeto está licenciado sob a Licença MIT - veja o arquivo LICENSE para mais detalhes.

### Agradecimentos

- Pomelo.EntityFrameworkCore.MySql
- Documentação do ASP.NET Core

