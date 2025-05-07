API de Logs
------------

Um projeto de API para registrar e consultar logs com Express e Node.js.

Como Funciona
-------------
Esta API tem duas funcionalidades principais:

1. Registrar logs com nome de aluno, gerando um ID único.
2. Consultar logs através do ID gerado.

Tecnologias
------------
- Node.js
- Express
- UUID (para gerar IDs únicos)

Como Rodar
-----------
1. Clone o repositório

   Abra o terminal e execute:

   git clone https://github.com/seu-usuario/api-logs.git
   cd api-logs

2. Instale as dependências

   Dentro do diretório do projeto, instale as dependências com o comando:

   npm install

3. Rodando o servidor

   Para rodar o servidor, execute:

   node script.js

   A API estará disponível em http://localhost:3000

1. POST /logs - Registrar Log
------------------------------
Envie o nome do aluno para registrar o log.

Exemplo de corpo da requisição:

{
  "nome": "Carlinhos Brown"
}

Resposta esperada:

{
  "mensagem": "Log registrado com sucesso.",
  "id": "uuid-gerado"
}

2. GET /logs/:id - Consultar Log por ID
---------------------------------------
Consulte um log pelo ID gerado.

Exemplo de URL:

http://localhost:8000/logs/uuid-gerado

Resposta esperada (se encontrado):

{
  "log": "uuid-gerado - 2025-05-07 12:13:11 - Carlinhos Brown"
}

Testando a API
---------------
Você pode testar a API usando o **Postman**
