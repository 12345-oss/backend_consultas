# API de Marcacao de Consultas

API REST em Java 17 com Spring Boot para cadastro de pacientes e especialidades medicas, com persistencia em banco H2 no modo arquivo. Projeto academico desenvolvido na FIAP.

## Tecnologias

Java 17, Spring Boot (Web MVC e Data JPA), H2 Database, Lombok e Maven.

## Arquitetura

O codigo segue divisao em camadas: `controller` expoe os endpoints REST, `service` concentra as regras de negocio, `repository` faz o acesso a dados via Spring Data JPA e `model` contem as entidades `Paciente` e `Especialidade`.

## Endpoints

Pacientes: `GET /pacientes`, `GET /pacientes/{id}`, `POST /pacientes`, `PUT /pacientes/{id}` e `DELETE /pacientes/{id}`.

Especialidades: `GET /especialidades`, `GET /especialidades/{id}`, `POST /especialidades`, `PUT /especialidades/{id}` e `DELETE /especialidades/{id}`.

## Como executar

Pre-requisito: Java 17 ou superior. Na raiz do projeto, execute `./mvnw spring-boot:run` (ou `mvnw.cmd spring-boot:run` no Windows).

A API sobe em http://localhost:8080 e o console do H2 fica em http://localhost:8080/h2-console, com usuario `sa` e senha vazia. Os arquivos do banco sao gravados em `./data/consultas`.

## Observacao

A pasta `target/` foi versionada por engano no commit inicial. Ela contem apenas artefatos de build e deve ser removida do repositorio; o `.gitignore` do projeto ja cobre esse caso.
