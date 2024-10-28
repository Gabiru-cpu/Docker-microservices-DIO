# Projeto de Microsserviços com Docker

Este projeto contém uma aplicação básica composta por dois microsserviços usando Docker: um banco de dados MySQL e um backend PHP. O backend permite a inserção de dados na tabela `mytable` no MySQL.

## Pré-requisitos

- Docker instalado na máquina
- Conhecimento básico de comandos Docker

## Estrutura do Projeto

- **docker-compose.yml**: Define os serviços para MySQL e PHP.
- **src/index.php**: Código PHP que insere uma nova entrada na tabela `mytable`.

## Como Executar

1. Clone o repositório e navegue até a pasta do projeto:
    ```bash
    git clone https://github.com/Gabiru-cpu/Docker-microservices-DIO.git
    cd Docker-microservices-DIO
    ```

2. Inicie os containers:
    ```bash
    docker-compose up -d
    ```

3. Verifique se os containers estão rodando:
    ```bash
    docker-compose ps
    ```

4. Acesse o backend em [http://localhost:8080](http://localhost:8080) para executar o script PHP e inserir uma nova entrada na tabela.

## Comandos Úteis

- Parar os containers:
    ```bash
    docker-compose down
    ```

- Ver logs de um container específico:
    ```bash
    docker logs php_container
    ```

## Estrutura do Banco de Dados

### Tabela `mytable`
Crie a tabela `mytable` no MySQL para o código PHP funcionar corretamente:
```sql
CREATE TABLE mytable (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(255) NOT NULL
);
