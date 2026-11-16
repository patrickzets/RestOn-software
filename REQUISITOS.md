# Requisitos do RestON: bibliotecas e versões

Fonte: `backend/pom.xml` e `frontend/package.json` do projeto RestON.

## Ferramentas no computador

| Ferramenta | Versão | Observação |
|---|---|---|
| Java (JDK) | 21 | `java.version` do `pom.xml` |
| Maven | 3.10.0 | Vem pelo Maven Wrapper (`mvnw`), não precisa instalar |
| Node.js | 24 ou mais novo | com npm 11 |
| PostgreSQL | 17 | banco `reston`, usuário `reston` |
| Docker Desktop | opcional | só se for subir o banco pelo `docker-compose.yml` |

## Backend (Java / Spring Boot)

Spring Boot **4.1.2** (`spring-boot-starter-parent`). As bibliotecas marcadas
com "Spring Boot" não têm versão própria: usam a que o Spring Boot 4.1.2 define.

### Dependências

| Biblioteca | Versão |
|---|---|
| spring-boot-starter-webmvc | Spring Boot 4.1.2 |
| spring-boot-starter-data-jpa | Spring Boot 4.1.2 |
| spring-boot-starter-security | Spring Boot 4.1.2 |
| spring-boot-starter-validation | Spring Boot 4.1.2 |
| spring-boot-starter-actuator | Spring Boot 4.1.2 |
| spring-boot-starter-flyway | Spring Boot 4.1.2 |
| flyway-database-postgresql | Spring Boot 4.1.2 |
| postgresql (driver, runtime) | Spring Boot 4.1.2 |
| spring-boot-devtools (runtime) | Spring Boot 4.1.2 |
| springdoc-openapi-starter-webmvc-ui | **3.2.0** |
| bcprov-jdk18on (BouncyCastle) | **1.86** |

### Testes

| Biblioteca | Versão |
|---|---|
| spring-boot-starter-webmvc-test | Spring Boot 4.1.2 |
| spring-boot-starter-data-jpa-test | Spring Boot 4.1.2 |
| spring-boot-starter-security-test | Spring Boot 4.1.2 |
| spring-boot-starter-validation-test | Spring Boot 4.1.2 |
| spring-boot-starter-actuator-test | Spring Boot 4.1.2 |
| spring-boot-starter-flyway-test | Spring Boot 4.1.2 |
| spring-boot-testcontainers | Spring Boot 4.1.2 |
| testcontainers-junit-jupiter | Spring Boot 4.1.2 |
| testcontainers-postgresql | Spring Boot 4.1.2 |

Os testes do backend usam Testcontainers, então precisam do Docker ligado.

## Frontend (Angular)

Versões como estão no `package.json` (`^` aceita atualizações compatíveis;
`~` aceita só correções).

### Dependências

| Biblioteca | Versão |
|---|---|
| @angular/common | ^21.2.0 |
| @angular/compiler | ^21.2.0 |
| @angular/core | ^21.2.0 |
| @angular/forms | ^21.2.0 |
| @angular/platform-browser | ^21.2.0 |
| @angular/router | ^21.2.0 |
| @fontsource-variable/geist | ^5.3.0 |
| @fontsource-variable/geist-mono | ^5.3.0 |
| rxjs | ~7.8.0 |
| tslib | ^2.3.0 |

### Desenvolvimento e testes

| Biblioteca | Versão |
|---|---|
| @angular/cli | ^21.2.29 |
| @angular/build | ^21.2.29 |
| @angular/compiler-cli | ^21.2.0 |
| typescript | ~5.9.2 |
| vitest | ^4.0.8 |
| jsdom | ^28.0.0 |
| @playwright/test | ^1.65.0 |
| prettier | ^3.8.1 |

## Como instalar

```
cd backend  && .\mvnw.cmd validate     # baixa o Maven e confere o pom.xml
cd frontend && npm install             # instala as bibliotecas do package.json
```
