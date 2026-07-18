# Employee and Department Many-to-One One-to-Many Mapping

## Overview
Create a Spring Boot application with two entities: "Employee" and "Department". An Employee can belong to only one Department, and a Department can have multiple Employees. Implement a one-to-many bidirectional mapping between these entities using Spring JPA. 

## Functional Requirements:
Create folders named controller, model, repository, and service inside the **employeedepartmentnto11ton/src/main/java/com/giftabled/employeedepartmentnto11ton**.

Inside the controller folder, create classes named "EmployeeController" and "DepartmentController". Inside the model folder,

Create a class named "Employee" with the following attributes:
1. employeeld - int(auto-generated primary key)
2. employeeName - String
3. designation - String
4. department - Department (ManyToOne, JsonBackReference)

Create another class named "Department" with the following attributes:
1. departmentld - int(auto-generated primary key)
2. departmentName - String
3. employees - List<Employee>(OneToMany, mappedBy = "department", Json Managed Reference)

Implement getters, setters, and constructors for the Employee and Department entities.

Inside the repository folder, create interfaces named "EmployeeRepo" and "DepartmentRepo".

Inside the service folder, create interfaces named "EmployeeService" and "DepartmentService".

Also, create classes Employee Servicelmpl and DepartmentServiceImpl and they should implement the Employee Service and DepartmentService.

## Project Structure
Refer to the below image for the project structure:

```text
└── src
    └── main
        ├── java
        │   └── com
        │       └── giftabled
        │           └── employeedepartmentnto11ton
        │               ├── controller
        │               │   ├── DepartmentController.java
        │               │   └── EmployeeController.java
        │               │
        │               ├── model
        │               │   ├── Department.java
        │               │   └── Employee.java
        │               │
        │               ├── repository
        │               │   ├── DepartmentRepo.java
        │               │   └── EmployeeRepo.java
        │               │
        │               ├── service
        │               │   ├── DepartmentService.java
        │               │   ├── DepartmentServiceImpl.java
        │               │   ├── EmployeeService.java
        │               │   └── EmployeeServiceImpl.java
        │               │
        │               └── SpringappApplication.java
        │
        └── resources
            └── application.properties
```

## API ENDPOINTS
- POST - "/department" - Returns response status 201 with department object on successful creation or else 500.
- POST - "/department/employee/{departmentid}" - Returns response status 201 with an employee object on successfully mapping the employee to the departmentld or else 500.
- GET - "/department" - Returns response status 200 with List<Department> with employee object on successful retrieval or else 500.
- PUT - "/employee/{employeeld}" - Returns response status 200 with updated employee object on successful updation or else 404.
- DELETE - "/employee/{employeeld}" - Returns response status 200 with String "Employee deleted successfully" on successful deletion or else "Employee not found with ID: " + employeeld.
