# Voll.med - API Rest em Java com Spring Boot

Este README fornece instruções para criar uma API Rest em Java usando o Spring Boot. A API incluirá operações CRUD (Create, Read, Update, Delete) que interagem com um banco de dados MySQL. Além disso, utilizaremos o Flyway como ferramenta de Migrations para gerenciar o esquema do banco de dados, o Bean Validation para realizar validações e implementaremos paginação dos dados da API.

## Pré-requisitos

Antes de iniciar o desenvolvimento da API, verifique se você possui os seguintes pré-requisitos instalados em seu ambiente de desenvolvimento:

- [Java 17](https://openjdk.java.net/projects/jdk/17/)
- [Maven](https://maven.apache.org/)
- [MySQL](https://dev.mysql.com/downloads/)
- [Docker](https://www.docker.com/get-started/)

## Configuração do Projeto

### 1. Iniciando um novo projeto

Você pode criar um novo projeto Spring Boot facilmente usando o Spring Initializr (https://start.spring.io/). Certifique-se de selecionar as seguintes opções ao configurar o projeto:

- Project: Maven Project
- Language: Java
- Spring Boot: 3.1.3 (ou a versão mais recente disponível)
- Java: 17
- Dependencies: Certifique-se de incluir as dependências apropriadas, como "Spring Web", "Spring Data JPA", "Bean Validation", "Flyway" e "MySQL Driver".

### 2. Configuração do Banco de Dados

No arquivo `application.properties` (ou `application.yml`), configure as informações de conexão com o banco de dados MySQL:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/seu_banco_de_dados
spring.datasource.username=seu_usuario
spring.datasource.password=sua_senha
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
```

### 3. Configuração do Flyway
O Flyway permite gerenciar as migrações do banco de dados. Crie um diretório db/migration na raiz do seu projeto e coloque os scripts SQL de migração lá. O Flyway executará automaticamente esses scripts durante a inicialização da aplicação.

### 4. Desenvolvimento dos Endpoints CRUD
Desenvolva os endpoints CRUD para suas entidades de domínio. Aqui estão alguns exemplos:

- Crie classes de modelo para suas entidades.
- Crie repositórios JPA para acessar os dados.
- Crie controladores REST para manipular solicitações HTTP e chamar métodos do serviço.
- Use Bean Validation para validar entradas de dados.
- Implemente paginação dos resultados usando parâmetros de consulta, por exemplo, page e size.

### 5. Executando a Aplicação
Você pode executar sua aplicação Spring Boot a partir da linha de comando usando o seguinte comando Maven:

```shell 
mvn spring-boot:run
```
Acesse a API no navegador ou através de ferramentas como o Postman ou Insomnia.

### 6. Contribuição
Sinta-se à vontade para contribuir com melhorias, correções de bugs ou novos recursos para este projeto. Basta criar um fork do repositório, fazer as alterações e enviar um pull request.

### 7. Licença
Este projeto é distribuído sob a licença MIT. Consulte o arquivo LICENSE para obter mais informações.
