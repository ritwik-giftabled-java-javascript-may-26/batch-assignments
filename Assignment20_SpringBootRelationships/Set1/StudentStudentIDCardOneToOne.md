# Student and StudentIDCard One-to-One Mapping

## Overview:
Create a Spring Boot application with two entities: "Student" and "StudentIDCard". A Student can have only one StudentIDCard. Implement a one-to-one mapping between these entities using Spring JPA 

## Functional Requirements:
Create folders named as controller, model, repository, and service inside the studentstudentidcardonetoone/src/main/java/com/examly/studentstudentidcardonetoone.

Inside the controller folder, create a class named "StudentController".

Inside the model folder, Create a class named "Student" with the following attributes
1. id - Long
2. name - String
3. studentIDCard - StudentIDCard (OneToOne)

Create another class named "StudentIDCard" with the following attributes
1. id - Long
2. cardNumber - String

Implement getters, setters, and constructors for the attributes of both the Student and StudentIDCard entities.

Inside the repository folder, create interfaces named "StudentRepository" and "StudentIDRepository".

Inside the service folder, create a class named "StudentService".

## Project Structure
Refer to the below image for the project structure:
## Project Structure

```text
src
└── main
    ├── java
    │   └── com
    │       └── examly
    │           └── studentstudentidcardonetoone
    │               ├── controller
    │               │   └── StudentController.java
    │               │
    │               ├── model
    │               │   ├── Student.java
    │               │   └── StudentIDCard.java
    │               │
    │               ├── repository
    │               │   ├── StudentIDRepository.java
    │               │   └── StudentRepository.java
    │               │
    │               ├── service
    │               │   └── StudentService.java
    │               │
    │               └── SpringappApplication.java
    │
    └── resources
        └── application.properties
```

## API ENDPOINTS:
- POST "/student" - Returns response status code 201 along with the student object, which includes details of the student's ID card. The request body should include the student object along with the student's ID card details.
- GET "/student" - Returns response status 200 with List<Student> object, which includes details of the student's ID card on successful retrieval or else 404.
- GET"/student/{id}" - Returns response status 200 with student object, which includes details of the student's ID card on successful retrieval or else 404.
- PUT"/student/{id}" - Returns response status 200 with updated student object, which includes details of the student's ID card on successful updation or else 404. The request body should include the student object along with the student's ID card details. All fields are modifiable except for the 'id' field.
- DELETE"/student/{id}" - Returns response status 200 with String "Deleted Student successfully" on successful deletion or else "Student with ID " +id+" not found".
