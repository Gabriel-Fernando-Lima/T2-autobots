# API Autobots — Atividade 2  

## Tecnologias Utilizadas
- Java 17  
- Spring Boot  
- Spring Web  
- Spring Data JPA  
- Spring HATEOAS  
- H2 Database  
- Lombok  
- Maven  

---

## Como Executar o Projeto

### Pré-requisitos
- JDK 17 instalado  
- Maven instalado  

### Rodar o projeto

- mvn spring-boot:run

### A API ficará disponível em:

- http://localhost:8080


# Endpoints da API

##A API contém quatro módulos principais, cada um com operações CRUD completas:

/cliente

/documento

/endereco

/telefone

## Cada seção abaixo contém os endpoints e JSONs de exemplo para testes em Postman/Thunder Client.

### 1. CLIENTE
GET /cliente/clientes

Retorna todos os clientes.

GET /cliente/{id}

Retorna um cliente pelo ID.

POST /cliente/cadastro

Cadastro de cliente.

Exemplo de JSON:
{
  "nome": "Nome Completo",
  "nomeSocial": "Nome Social",
  "dataNascimento": "2000-01-01",
  "dataCadastro": "2023-01-01",
  "documentos": [
    {
      "tipo": "RG",
      "numero": "123456789"
    }
  ],
  "endereco": {
    "estado": "SP",
    "cidade": "Cidade Exemplo",
    "bairro": "Centro",
    "rua": "Rua das Flores",
    "numero": "100",
    "codigoPostal": "12345-000",
    "informacoesAdicionais": "Bloco A"
  },
  "telefones": [
    {
      "ddd": "12",
      "numero": "999999999"
    }
  ]
}

PUT /cliente/atualizar

Atualização de cliente.

Exemplo de JSON:
{
  "id":"1",
  "nome": "Nome Atualizado",
  "nomeSocial": "Nome Social Atualizado",
  "dataNascimento": "9999-99-99",
  "dataCadastro": "9999-99-99"
}

DELETE /cliente/excluir

Exclui o cliente especificado.

Exemplo de JSON:
{
  "id":"1"
}

### 2. DOCUMENTO
GET /documento/documentos

Retorna todos os documentos.

GET /documento/{id}

Retorna um documento pelo ID.

POST /documento/cadastro

Cadastro de documento.

Exemplo de JSON:
{
  "tipo": "CPF",
  "numero": "00011122233"
}

PUT /documento/atualizar

Atualização de documento.

Exemplo de JSON:
{
  "id":"1",
  "tipo": "CPF",
  "numero": "99984124127"
}

DELETE /documento/excluir

Remove o documento informado.

Exemplo de JSON:
{
  "id":"1"
}

### 3. ENDERECO
GET /endereco/enderecos

Retorna todos os endereços.

GET /endereco/{id}

Retorna um endereço pelo ID.

POST /endereco/cadastro

Cadastro de endereço.

Exemplo de JSON:
{
  "estado": "SP",
  "cidade": "São José dos Campos",
  "bairro": "Centro",
  "rua": "Rua Principal",
  "numero": "200",
  "codigoPostal": "12000-000",
  "informacoesAdicionais": "Casa 2"
}

PUT /endereco/atualizar

Atualização de endereço.

Exemplo de JSON:
{
  "id":"1"
  "cidade": "Cidade Atualizada",
  "rua": "Nova Rua"
}

DELETE /endereco/excluir

Remove o endereço informado.

Exemplo de JSON:
{
  "id":"1"
}


### 4. TELEFONE
GET /telefone/telefones

Retorna todos os telefones.


GET /telefone/{id}

Retorna um telefone pelo ID.


POST /telefone/cadastro

Cadastro de telefone.

Exemplo de JSON:
{
  "ddd": "12",
  "numero": "988887777"
}


PUT /telefone/atualizar

Atualização de telefone.

Exemplo de JSON:
{
  "id":"1",
  "ddd": "11",
  "numero": "977777777"
}


DELETE /telefone/{id}

Remove o telefone informado.

Exemplo de JSON:
{
  "id":"1"
}
