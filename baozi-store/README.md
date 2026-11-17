# Baozi Store - API REST

API REST para controle de clientes, produtos e pedidos de uma loja de pao chines.
Trabalho da disciplina Desenvolvimento Web Back-End.

## Tecnologias
Java 17, Spring Boot 3, Spring Data JPA, H2 (ou MySQL), Maven.

## Como rodar
```
mvn spring-boot:run
```
A API sobe em `http://localhost:8080`. Console do H2: `http://localhost:8080/h2-console`
(JDBC URL: `jdbc:h2:mem:baozi`, usuario `sa`, senha vazia).

## Endpoints

| Metodo | Rota | Descricao |
|---|---|---|
| POST | /clientes, /produtos, /pedidos | Cria |
| GET | /clientes, /produtos, /pedidos | Lista todos |
| GET | /{entidade}/{id} | Consulta por ID |
| DELETE | /{entidade}/{id} | Apaga |

Exemplo de corpo para criar pedido:
```json
{ "clienteId": 1, "produtoId": 1, "quantidade": 3 }
```
