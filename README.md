📋 API de Gerenciamento de Tarefas

API RESTful desenvolvida em Node.js para o gerenciamento de tarefas com funcionalidades completas de CRUD, filtros, validação, logs e estrutura modular seguindo o padrão MVC simplificado.
🚀 Tecnologias Utilizadas

    Node.js

    Express

    Joi

    UUID

    Morgan (opcional)

    JavaScript (ES6+)

🗂️ Estrutura de Pastas

api-tarefas/
├── src/
│   ├── controllers/
│   │   └── tarefasController.js
│   ├── routes/
│   │   └── tarefasRoutes.js
│   ├── services/
│   │   └── tarefasService.js
│   ├── middlewares/
│   │   └── validateTarefa.js
│   ├── utils/
│   │   └── logger.js
│   ├── database/
│   │   └── fakeDb.js
│   └── app.js
├── package.json
└── README.md

🛠️ Instalação e Execução

    Clone o repositório:

git clone https://github.com/seu-usuario/api-tarefas.git
cd api-tarefas

    Instale o Node.js:
    https://nodejs.org

    Instale as dependências:

npm install express joi uuid morgan

    Inicie o servidor:

node src/app.js

O servidor será iniciado em http://localhost:3000.
📌 Endpoints Disponíveis
Método	Rota	Descrição
GET	/tarefas	Lista todas as tarefas
GET	/tarefas?concluida=true	Lista apenas tarefas concluídas
GET	/tarefas/:id	Retorna uma tarefa específica
POST	/tarefas	Cria uma nova tarefa
PUT	/tarefas/:id	Atualiza todos os campos da tarefa
PATCH	/tarefas/:id/concluir	Marca a tarefa como concluída
DELETE	/tarefas/:id	Remove uma tarefa
✅ Validações

    Campos obrigatórios: titulo, descricao, concluida

    Título: Mínimo de 3 caracteres

    Validação feita via middleware usando o pacote Joi

🧠 Funcionalidades Implementadas

    CRUD completo de tarefas

    Filtro por query parameter (concluida)

    Filtro por path parameter (:id)

    Middleware de validação

    Estrutura modular em camadas (Controller, Service, Middleware)

    Banco de dados simulado (fakeDb.js)

    Tratamento global de erros com mensagens claras

    Sistema de log simples (logger.js)

🧪 Testes

Use Postman para testar os endpoints.
Certifique-se de enviar os dados corretos no corpo da requisição, por exemplo:
POST /tarefas

{
  "titulo": "Estudar Node.js",
  "descricao": "Focar em estrutura de API REST",
  "concluida": false
}

🔍 Logs do Sistema

As ações são registradas no console:

    "Tarefa criada com sucesso."

    "Tentativa de criação com dados inválidos."

    "Tarefa deletada."

    E outros logs informativos

