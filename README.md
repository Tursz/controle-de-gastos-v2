# 💰 Controle de Gastos com Spring Boot e HTMX

Versão: *v2.1*

## 📋 Descrição

Aplicação *full-stack* para controle de despesas e receitas pessoais.  
Permite *criar, editar e excluir lançamentos financeiros* com interface dinâmica, sem recarregar a página inteira, usando *HTMX* e *Thymeleaf*.  

O *backend* é feito em *Spring Boot/Java, com persistência via **JPA, banco de dados **H2* para desenvolvimento e *PostgreSQL* para produção.  
A aplicação é empacotada com *Docker* para fácil deploy.

---

## 🛠 Tecnologias Utilizadas

- *Java 21*
- *Spring Boot* (Web, Data JPA, DevTools)
- *Thymeleaf* + *HTMX*
- *H2 Database* (Dev)
- *PostgreSQL* (Prod)
- *Docker* (Deploy)

---

## 🏗 Arquitetura

- *MVC (Model-View-Controller)*
- *Controllers* recebem requisições HTTP e chamam os repositórios
- *Views* renderizadas com Thymeleaf
- *HTMX* para interações dinâmicas (requisições parciais, atualização de trechos da página)
- *Perfis de ambiente* para desenvolvimento e produção (H2 x PostgreSQL)

---

## 📂 Estrutura do Projeto

```bash
controle-de-gastos/
├── src/
│   ├── main/
│   │   ├── java/br/com/controledegastos/
│   │   │   ├── ControleDeGastosApplication.java
│   │   │   ├── controller/
│   │   │   ├── model/
│   │   │   └── repository/
│   │   └── resources/
│   │       ├── templates/
│   │       ├── application.properties
│   │       └── application-prod.properties
│   └── test/
├── Dockerfile
├── pom.xml
└── mvnw, mvnw.cmd
