                                                                        CRUD Project.

Product API

The Product API is a RESTful web service built with Spring Boot that provides CRUD (Create, Read, Update, Delete) 
operations for managing products. This API is documented using Swagger (OpenAPI), allowing you to easily explore and test the endpoints.

CRUD operations for products
Input validation
Global exception handling
API documentation with Swagger UI

Configure the Database

#application.properties File
spring.datasource.url=jdbc:mysql://localhost:3306/product
spring.datasource.username=root
spring.datasource.password=root
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQL8Dialect
                                                              
															                                                  API Endpoints
															  
GET /products
Description: Retrieves a list of all products.
Response: 200 OK with the list of products.


GET /products/{id}
Description: Retrieves a product by its ID.
Response:
200 OK with the product details if found.
404 Not Found if the product does not exist.


POST /products
Description: Creates a new product.
Request Body: JSON representation of the product.
Response:
201 Created with the created product.
400 Bad Request if the input is invalid

PUT /products/{id}
Description: Updates an existing product by its ID.
Request Body: JSON representation of the updated product.
Response:
200 OK with the updated product.
404 Not Found if the product does not exist.
400 Bad Request if the input is invalid


DELETE /products/{id}
Description: Deletes a product by its ID.
Response:
204 No Content if the product is deleted successfully.
404 Not Found if the product does not exist.
