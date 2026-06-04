# HibernateIntro
Created book database in mysql local DB and test the functionality using following commands:
*Add books:
curl --location 'http://localhost:8080/saveBook' \
--header 'Content-Type: application/json' \
--data '{
    "title": "Spring Boot Essentials",
    "author":"John Doe",
    "price": 19.99
}
'
curl --location 'http://localhost:8080/saveBook' \
--header 'Content-Type: application/json' \
--data '{
    "title": "Hibernate in Depth",
    "author": "Michael Brown",
    "price": 22.00
}'
curl --location 'http://localhost:8080/saveBook' \
--header 'Content-Type: application/json' \
--data '{
    "title": "Effective Java",
    "author": "Joshua Bloch",
    "price": 28.99
}'
curl --location 'http://localhost:8080/saveBook' \
--header 'Content-Type: application/json' \
--data '{
    "title": "Clean Code",
    "author": "Robert C. Martin",
    "price": 25.75
}'
*List all books
curl --location 'http://localhost:8080/getBooks' or curl --location 'http://localhost:8080/getBooks' | jq
*get book by id: curl --location 'http://localhost:8080/getBook/1'
*Update book by id:
curl --location --request PUT 'http://localhost:8080/updateBook/1' \
--header 'Content-Type: application/json' \
--data '{"title":"SpringBoot","author": "John", "price":"10"}'
*Delete book by id:
curl --location --request DELETE 'http://localhost:8080/deleteBook/4'

** Also check the DB for the updated information.

