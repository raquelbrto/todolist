# todo-list
 API de tarefas todo list com:
 - Spring Boot.
 - Spring MVC
 - Spring Data JPA
 - Spring Doc 
 - MySql

### Requisitos

 - Usar banco de dados
 - Campos mínimos da entidade de tarefa 
 - Nome
 - Descrição
 - Realizado
 - Prioridade
 - Criar CRUD de tarefas

## Recursos necessarios para rodar a aplicação:
- IDE de sua preferencia
- Java 17
- SGBD MySql
- Configure o arquivo application.properties de acordo com a configuração do seu usuario do banco

## Como executar:
Na sua maquina clone o repositorio git:

        git clone https://github.com/raquelbrto/todolist.git

## Para acessar a documentação dos endpoints:
    http://localhost:8080/swagger-ui/index.html

## Endpoints
- Criar tarefa

        curl -X POST "localhost:8080/todos" -H 'Content-Type: application/json' -d'

        {
        "nome" : "Todo 4",
        "descricao" : "teste",
        "prioridade" : 4
        
        }'

- Listar tarefas

        curl -X GET "localhost:8080/todos?pretty" -H 'Content-Type: application/json'

- Atualizar tarefa
        
        curl -X PUT "localhost:8080/todos?pretty" -H 'Content-Type: application/json' -d'

        {
        "nome" : "Todo 4",
        "descricao" : "teste",
        "prioridade" : 4
        
        }'

- Deletar tarefa

        curl -X DELETE "localhost:8080/todos/1" -H 'Content-Type: application/json'