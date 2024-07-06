# Menu Application Backend

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=java&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-F2F4F9?style=for-the-badge&logo=spring-boot)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![Lombok](https://img.shields.io/badge/Lombok-ffffff?style=for-the-badge&logo=lombok&logoColor=black)

## Descrição

O Menu Application Backend é uma API RESTful desenvolvida com Java e Spring Boot que gerencia um menu de alimentos. Ele oferece endpoints para realizar operações CRUD (Create, Read, Update, Delete) em um menu de alimentos armazenados em um banco de dados PostgreSQL.

## Tecnologias Utilizadas

- **Java**
- **Spring Boot**
- **Spring Data JPA**
- **PostgreSQL**
- **Lombok**

## Funcionalidades

- Listar todos os itens do menu.
- Adicionar novos itens ao menu.
- Atualizar itens existentes.
- Remover itens do menu.

## Como Rodar o Projeto

### Pré-requisitos

- **Java 11** ou superior
- **Maven**
- **PostgreSQL**

### Passo a Passo

1. **Clone o repositório**

   ```bash
   git clone https://github.com/fermarino/menu-application-backend.git
   cd menu-application
   ```

2. **Configuração do Banco de Dados**

   Crie um banco de dados no PostgreSQL:

   ```sql
   CREATE DATABASE food;
   ```

3. **Configure o banco de dados PostgreSQL e atualize o arquivo application.properties com suas credenciais**

   ```properties
   spring.datasource.url=jdbc:postgresql://localhost:5432/food
   spring.datasource.username=seu_usuario
   spring.datasource.password=sua_senha
   spring.jpa.hibernate.ddl-auto=update
   spring.jpa.show-sql=true
   spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.PostgreSQLDialect
   ```

4. **Compile e execute o projeto**

   No diretório raiz do projeto, execute o comando para compilar o projeto com Maven:

   ```bash
   mvn clean install
   ```

   Para iniciar a aplicação, execute o comando:

   ```bash
   mvn spring-boot:run
   ```

5. **Acesse a aplicação**

   A API estará disponível no endereço: `http://localhost:8080/food`

### Endpoints

- **GET /food**: Retorna a lista de todos os alimentos.
- **POST /food**: Insere um novo alimento.