API de Logs
Uma API simples para registrar e consultar logs com Express e Node.js.

Como Funciona
Essa API permite:

Registrar logs com nome do aluno, gerando um ID único.

Consultar logs através do ID gerado.

Tecnologias
Node.js

Express

UUID (para gerar IDs únicos)

Como Rodar
1. Clone o repositório
bash
Copiar
Editar
git clone https://github.com/seu-usuario/api-logs.git
cd api-logs
2. Instale as dependências
bash
Copiar
Editar
npm install
3. Rodando o servidor
bash
Copiar
Editar
node script.js
Agora, a API estará rodando em http://localhost:3000.

Endpoints
1. POST /logs - Registrar Log
Envie o nome do aluno e registre o log:

Exemplo de corpo da requisição:

json
Copiar
Editar
{
  "nome": "João da Silva"
}
Resposta esperada:

json
Copiar
Editar
{
  "mensagem": "Log registrado com sucesso.",
  "id": "uuid-gerado"
}
2. GET /logs/:id - Consultar Log por ID
Consulte um log pelo ID gerado:

Exemplo de URL:

bash
Copiar
Editar
http://localhost:3000/logs/uuid-gerado
Resposta esperada (se encontrado):

json
Copiar
Editar
{
  "log": "uuid-gerado - 2025-05-07 12:13:11 - João da Silva"
}
Testando
Você pode testar a API com o Postman ou usando cURL diretamente no terminal.

Exemplo cURL para registrar um log:

bash
Copiar
Editar
curl -X POST http://localhost:3000/logs -H "Content-Type: application/json" -d '{"nome": "João da Silva"}'
Exemplo cURL para consultar um log:

bash
Copiar
Editar
curl http://localhost:3000/logs/uuid-gerado
Licença
MIT
