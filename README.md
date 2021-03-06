# Exemplo de API rodando em Container Docker

Esta é uma API simples rodando dentro de um container Docker

# Requisitos

-   Node.js com NPM
-   Git
-   Docker

# Como rodar a API

Execute os comandos abaixo para que a aplicação rode na sua máquina:

### Clonar o repositório

```
git clone <https://github.com/Herley25/api>
```

### Entrar no diretório do projeto

```
cd api_teste
```

### Instalar as dependências do projeto

```
npm install
```

### Criar imagem Docker

```
docker build -t api_teste:1.0.0 .
```

### Rodar a API no Container

```
docker run -p 8080:8080 -d api_teste:1.0.0
```

### Acessar a API

Para acessar os métodos da API você poderá usar o POSTMAN:

-   `GET http://localhost:8080/produtos` retornar uma lista de produtos
-   `POST http://localhost:8080/produtos` criar um novo produto

### Payload

Para criar ou atualizar um novo produto você necessita enviar o Payload abaixo no body do método POST:

```json
{
    "nome": "API REST",
    "fabricante": "Datenworks",
    "aprendiz": "Herley"
}
```
