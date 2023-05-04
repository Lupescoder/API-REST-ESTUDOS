# API Rest com Spring Boot e MySQL

Este projeto tem como objetivo apresentar um exemplo simples de como criar uma API Rest usando Spring Boot e MySQL. Ele foi desenvolvido como parte do meu aprendizado sobre o assunto e pode ser usado como ponto de partida para a criação de outros projetos.

## Requisitos

- Java 11 ou superior
- MySQL 8 ou superior
- Maven

## Configuração do ambiente

1. Clone o repositório para o seu computador
2. Crie um banco de dados MySQL com o nome `hospitais` (ou qualquer outro nome de sua preferência)
3. Configure as credenciais de acesso ao banco de dados no arquivo `application.properties`
4. Execute o comando `mvn clean install` para instalar as dependências e gerar o arquivo `.jar`

## Utilização

Para executar a API, basta executar o arquivo `.jar` gerado pelo comando `mvn clean install`. A API será iniciada na porta 8080.

### Endpoints

- `GET /medicos`: Retorna todos os medicos cadastradas no banco de dados
- `POST /medicos`: Cria um novo medico com base nos dados enviados no corpo da requisição
- `GET /pacientes`: Retorna todas os pacientes cadastradas no banco de dados
- `POST /pacientes`: Cria um novo paciente com base nos dados enviados no corpo da requisição


### Exemplo de requisição

```http
POST /medicos HTTP/1.1
Host: localhost:8080
Content-Type: application/json

{
    "nome": "João da Silva",
    "email": "testeMedico@gmail.com",
    "crm": "12345",
    "especialidade": "CARDIOLOGISTA",
    "endereco": {
        "bairro": "Asa Norte",
        "numero": 404,
        "complemento": "Proximo ao Patio"
  }
}
