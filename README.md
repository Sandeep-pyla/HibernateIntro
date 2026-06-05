# HibernateIntro

Hibernate is an open-source ORM framework for Java. It helps persist and retrieve Java objects from relational databases.

## Key Benefits
- Automates SQL query generation
- Supports lazy and eager loading
- Handles One-to-Many and Many-to-Many relationships
- Supports caching for better performance

---

## Key Components of Hibernate

| Component        | Description |
|------------------|-------------|
| SessionFactory   | Creates Hibernate sessions and manages configurations |
| Session          | Handles database operations for entities |
| Transaction      | Ensures atomicity of database changes |
| Query            | Executes HQL (Hibernate Query Language) or SQL queries |
| Entity Classes   | POJOs mapped to database tables |
| Configuration    | Loads Hibernate settings from `hibernate.cfg.xml` |

---

## Creating and Testing Data

Created a `book` database in MySQL local DB and tested functionality using the following APIs.

---

## Add Books

```bash
curl --location "http://localhost:8080/saveBook" \
--header "Content-Type: application/json" \
--data '{
  "title": "Spring Boot Essentials",
  "author": "John Doe",
  "price": 19.99
}'

```list all books
curl --location "http://localhost:8080/getBooks"

```get book by id
curl --location "http://localhost:8080/getBook/1"

```update book by id
curl --location --request PUT "http://localhost:8080/updateBook/1" \
--header "Content-Type: application/json" \
--data '{
  "title": "SpringBoot",
  "author": "John",
  "price": 10
}'

```delete book by id
curl --location --request DELETE "http://localhost:8080/deleteBook/4"