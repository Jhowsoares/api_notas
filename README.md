Descrição da API
A API Notas permite gerenciar notas de alunos por meio de operações CRUD completas. Com ela, é possível listar, criar, consultar, atualizar e remover notas, utilizando autenticação via Bearer Token (JWT). A API segue o padrão OpenAPI 3.0.0 e retorna respostas em JSON.


Endpoints
GET /notas
Lista todas as notas cadastradas com suporte a paginação.

POST /notas
Cria uma nova nota para um aluno.

GET /notas/{id}
Retorna os detalhes de uma nota específica.

PUT /notas/{id}
Atualiza os dados de uma nota existente.

DELETE /notas/{id}

Remove uma nota do sistema.


Documentação no GitHub Pages

https://SEU-USUARIO.github.io/notas-api/