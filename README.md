🌐 API Gateway - Microsserviço de Acesso

✨ Visão Geral

Este é o microsserviço API Gateway, que atua como o ponto de entrada unificado para a aplicação de lista de tarefas. Sua principal função é receber as requisições HTTP (REST) do frontend, traduzi-las para chamadas gRPC e encaminhá-las para o Task Service (e outros futuros microsserviços de backend). Ele também processa as respostas gRPC e as retorna ao frontend em formato REST.

🚀 Funcionalidades

O API Gateway expõe uma API REST para o frontend, incluindo endpoints para:

    GET /tasks: Lista todas as tarefas.

    POST /tasks: Cria uma nova tarefa.

    PUT /tasks/:id: Atualiza uma tarefa existente.

    DELETE /tasks/:id: Exclui uma tarefa.

🛠️ Tecnologias Utilizadas

    Node.js: Ambiente de execução.

    TypeScript: Linguagem de programação para tipagem estática.

    Express.js: Framework web para construir a API REST.

    gRPC: Protocolo de comunicação utilizado para interagir com o Task Service.

    @grpc/grpc-js: Cliente gRPC para Node.js.

⚙️ Configuração e Execução Local

Para rodar o API Gateway no seu ambiente local, siga os passos abaixo:

Pré-requisitos

Certifique-se de ter os seguintes softwares instalados:

    Node.js (versão 18 ou superior recomendada)

    npm (gerenciador de pacotes do Node.js)

    O Task Service deve estar em execução na porta 50051.

1. Configuração das Variáveis de Ambiente (.env)

Crie um arquivo chamado .env na raiz deste diretório (api-gateway/) e adicione as seguintes variáveis:
Snippet de código

API_GATEWAY_PORT=3000
TASK_SERVICE_URL=localhost:50051

Importante: Este arquivo .env já está no .gitignore e NÃO deve ser enviado para o GitHub.

2. Instalação das Dependências

Com o terminal aberto na raiz do diretório api-gateway/, instale as dependências do projeto:
Bash

npm install

3. Execução do Serviço

Para iniciar o API Gateway em modo de desenvolvimento (com recarregamento automático):
Bash

npm run start:dev

O serviço será iniciado na porta 3000 (conforme API_GATEWAY_PORT no .env). Você verá mensagens de log indicando que o servidor Express está pronto para receber requisições.

🤝 Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou pull requests caso encontre problemas ou queira adicionar funcionalidades.

📄 Licença

Este projeto está licenciado sob a MIT License.
