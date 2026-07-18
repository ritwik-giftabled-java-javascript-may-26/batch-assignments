# Customer and Product Many-to-One Mapping

## Overview:
Create a Spring Boot application with two entities: "Customer" and "Product". A customer can have multiple products. Implement a Many-to-One undirectional mapping between these entities using Spring JPA. 

## Functional Requirements:
Create folders named controller, model, repository, and service inside the **customerproductmanytoone/src/main/java/com/giftabled/customerproductmanytoone**.

Inside the controller folder, create classes named "CustomerController" and "ProductController".

Inside the model folder, Create a class named "Customer" with the following attributes:
1. customerld - int(auto-generated primary key)
2. customerName - String
3. address - String

Create another class named "Product" with the following attributes:
1. productid - int(auto-generated primary key)
2. productName - String
3. price - double
4. customer - Customer(ManyToOne)

Implement getters, setters, and constructors for the Team and Player entities.

Inside the repository folder, create interfaces named "CustomerRepo" and "ProductRepo".

Inside the service folder, create interfaces named "CustomerService" and "ProductService".

Also, create classes CustomerServicelmpl and ProductServicelmpl and it should implement the CustomerService and ProductService.

## Project Structure
Refer to the below image for the project structure:

```text
src
└── main
    ├── java
    │   └── com
    │       └── giftabled
    │           └── customerproductmanytoone
    │               ├── controller
    │               │   ├── CustomerController.java
    │               │   └── ProductController.java
    │               │
    │               ├── model
    │               │   ├── Customer.java
    │               │   └── Product.java
    │               │
    │               ├── repository
    │               │
    │               ├── service
    │               │   ├── CustomerService.java
    │               │   ├── CustomerServiceImpl.java
    │               │   ├── ProductService.java
    │               │   └── ProductServiceImpl.java
    │               │
    │               └── SpringappApplication.java
    │
    └── resources
        └── application.properties
```

## API ENDPOINTS
- POST - "/customer" - Returns response status 201 with customer object on successful creation or else 400.
- POST - "/product/customer/{customerld}" - Returns response status 201 with a product object on successfully mapping the product to the customerld or else 400.
- GET - "/customer/{customerld}" - Returns response status 200 with customer object on successful retrieval or else 404.
- GET - "/product/customer/{customerld}"- Returns response status 200 with List<Product> associated with the specified customerld or else 404.
- DELETE - "/product/{productid} - Returns response status 200 with String "Product deleted successfully" on successful deletion or else 404 "Product not found with ID "+productid.
