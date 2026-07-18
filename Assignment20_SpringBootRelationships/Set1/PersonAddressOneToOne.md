# Person and Address One-to-One Mapping

## Overview:
Create a Spring Boot application with two entities: "Person" and "Address". A person can have only one address. Implement a one-to-one mapping between these entities using Spring JPA 

## Functional Requirements:
Create folders named as controller, model, repository, and service inside the personaddressonetoone/src/main/java/com/giftabled/personaddressonetoone.

Inside the controller folder, create classes named "PersonController" and "AddressController".

Inside the model folder, Create a class named "Person" with the following attributes
1. id - Long (GeneratedValue)
2. name - String
3. email - String
4. phoneNumber - String
5. nationality String
6. address - Address (OneToOne)
   
Create another class named "Address" with the following attributes
1. id - Long (GeneratedValue)
2. street - String
3. city - String
4. zipCode - String

Implement getters, setters, and constructors for the Person and Address entities.

Inside the repository folder, create interfaces named "PersonRepository" and "AddressRepository".

Inside the service folder, create classes named "PersonService" and "AddressService".

## Project Structure
Refer to the below image for the project structure:

```text
src
└── main
    └── java
        └── com
            └── giftabled
                └── personaddressonetoone
                    ├── controller
                    │   ├── AddressController.java
                    │   └── PersonController.java
                    │
                    ├── model
                    │   ├── Address.java
                    │   └── Person.java
                    │
                    ├── repository
                    │   ├── AddressRepository.java
                    │   └── PersonRepository.java
                    │
                    ├── service
                    │   ├── AddressService.java
                    │   └── PersonService.java
                    │
                    └── SpringappApplication.java
```

## API ENDPOINTS:
- POST "/person" - Returns response status 201 with person object on successful creation or else 500.
- POST "/address/person/{personld}" - Returns response status 201 with address object on successfully mapping the address to the personld or else 500. 
- GET "/person" - Returns response status 200 with List<Person> object, which includes details of the address on successful retrieval or else 404. 
- GET"/person/{personld}" - Returns response status 200 with person object, which includes details of the address on successful retrieval or else 404.
