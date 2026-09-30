# Spring Boot Sample

A minimal Spring Boot REST API created as a learning sample.

## Tech Stack

- Java 17
- Spring Boot 3.5.6
- Spring Web
- Maven

## Project Flow

```
Client
  ↓
HelloController
  ↓
Response
```

## Endpoint

```
GET /api/hello
```

Response:

```
Hello from Spring Boot!
```

## Run

```bash
mvn spring-boot:run
```

Then open:

```
http://localhost:8080/api/hello
```
