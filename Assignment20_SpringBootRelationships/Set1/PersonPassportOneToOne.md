# Person and Passport One-To-One Mapping

## Overview:
Create a Spring Boot application with two entities: "Person" and "Passport". A person can have only one passport and a passport can belong to only one person. Implement a one-to-one mapping between these entities using Spring JPA. 

## Functional Requirements:
Create folders named as controller, model, repository, and service inside the personpassportonetoone/src/main/java/com/giftabled/personpassportonetoone.

Inside the controller folder, create classes named "PassportController" and "PersonController".

Inside the model folder, Create a class named "Passport" with the following attributes
1. id - Long (auto-generated)
2. serialNumber-String
3. issueYear - int
4. country - String

Create another class named "Person" with the following attributes
1. id - Long (auto-generated)
2. name - String
3. dateOfBirth - String
4. email - String
5. phoneNumber - String
6. passport - Passport (OneToOne)
   
Implement getters, setters, and constructors for the attributes of both the Passport and Person entities.

Inside the repository folder, create interfaces named "PassportRepository" and "PersonRepository".

Inside the service folder, create classes named "PassportService" and "PersonService".

## Project Structure
Refer to the below image for the project structure:

## Project Structure

```text
src
└── main
    ├── java
    │   └── com
    │       └── giftabled
    │           └── personpassportonetoone
    │               ├── controller
    │               │   ├── PassportController.java
    │               │   └── PersonController.java
    │               │
    │               ├── model
    │               │   ├── Passport.java
    │               │   └── Person.java
    │               │
    │               ├── repository
    │               │   ├── PassportRepository.java
    │               │   └── PersonRepository.java
    │               │
    │               ├── service
    │               │   ├── PassportService.java
    │               │   └── PersonService.java
    │               │
    │               └── SpringappApplication.java
    │
    └── resources
        └── application.properties
```

## API ENDPOINTS:
- POST - "/passport" - Returns response status 201 with passport object on successful creation or else 400.
- POST-"/person/passport/{passportid}" - Returns response status 201 with person object on successfully mapping the person to the passportid or else 400. 
- GET-"/person/{personld}" - Returns response status 200 with person object, which includes details of the passport on successful retrieval or else 404. 
- GET-"/passport"- Returns response status 200 with List<Passport> object on successful retrieval or else 404.
GET-"/person/search/name?name={name}" - Returns response status 200 with a List<Person> objects matching the search criteria, or 404 if no persons are found. GET-"/person/search/email?email={email}" - Returns response status 200 with a List<Person> objects matching the search criteria, or 404 if no persons are found.
