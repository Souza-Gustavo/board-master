# Board de Tarefas em Java

Um aplicativo de console simples para gerenciamento de tarefas (board), desenvolvido como desafio da DIO. Permite criar, listar, editar e remover tarefas com status definido, utilizando Java puro e conexão com banco de dados MySQL.

---

##  Projeto

Este projeto implementa um board de tarefas em Java com operações CRUD básicas (criar, listar, editar e remover). Ele serve como aprendizado prático de:

- Programação orientada a objetos (POO) em Java
- Conexão com banco de dados via JDBC/MySQL
- Boas práticas de modularização em pacotes (`model`, `repository`, etc.)

Objetivo: consolidar o entendimento de arquitetura simples em aplicações Java com persistência.

---

##  Tecnologias

- **Java 21**
- **MySQL** (versão recomendada: 8+)
- **JDBC (Connector/J)** para conexão com o banco
- **Lombok** para redução de boilerplate (como `@NoArgsConstructor`)

---

##  Pré-requisitos

Antes de rodar o projeto, você deve ter instalado em sua máquina:

- Java 21 ou superior
- MySQL instalado e um servidor ativo
- Um banco chamado `board` criado com um usuário `board` adequadamente configurado

---

##  Instalação e configuração

1. Clone este repositório:
    ```bash
    git clone <URL_DO_REPO>
    cd board-master
    ```

2. Crie o banco de dados e usuário MySQL (exemplo):
    ```sql
    CREATE DATABASE board;
    CREATE USER 'board'@'localhost' IDENTIFIED BY 'board';
    GRANT ALL PRIVILEGES ON board.* TO 'board'@'localhost';
    FLUSH PRIVILEGES;
    ```

3. Ajuste o `ConnectionConfig`, se necessário, para garantir que se conecte corretamente ao MySQL. Substitua `localhost` por `127.0.0.1`, especifique a porta (geralmente `3306`), e adicione parâmetros como `useSSL=false` e `serverTimezone=UTC` se necessário.

4. Compile e execute o projeto:
    ```bash
    javac -cp .;path\to\mysql-connector.jar br/com/dio/Main.java
    java -cp .;path\to\mysql-connector.jar br.com.dio.Main
    ```

Se estiver usando build tools como Maven ou Gradle, adapte os passos de compilação normalmente.

---
