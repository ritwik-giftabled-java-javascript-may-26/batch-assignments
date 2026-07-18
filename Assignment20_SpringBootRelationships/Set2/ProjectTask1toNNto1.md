# Project and Task One-to-Many Many-to-One Mapping

## Overview:
Create a Spring Boot application with two entities: "Project" and "Task". Each projects can have multiple tasks. Implement a one-to-many bidirectional mapping between these entities using Spring JPA. 

## Functional Requirements:
Create folders named controller, model, repository, and service inside the **projecttask1tonnto1/src/main/java/com/giftabled/projecttask1tonnto1**.

Inside the controller folder, create classes named "ProjectController" and "TaskController".

Inside the model folder, Create a class named "Project" with the following attributes:
1. projectld - int(auto-generated, primary key)
2. projectName -String
3. tasks - List<Task>(OneToMany, mappedBy = "project", JsonManagedReference)

Create another class named "Task" with the following attributes:
1. taskid - int(auto-generated, primary key)
2. title - String
3. description - String
4. completed - boolean
5. project - Project (ManyToOne, JsonBackReference)
   
Implement getters, setters, and constructors for the Project and Task entities.

Inside the repository folder, create interfaces named "ProjectRepository" and "TaskRepository.

Inside the service folder, create interfaces named "ProjectService" and "TaskService".

Also, create classes ProjectServiceImpl and TaskServicelmpl and they should implement the ProjectService and TaskService.

## Project Structure
Refer to the below image for the project structure:

```text
src
└── main
    ├── java
    │   └── com
    │       └── giftabled
    │           └── projecttask1tonnto1
    │               ├── controller
    │               │   ├── ProjectController.java
    │               │   └── TaskController.java
    │               │
    │               ├── model
    │               │   ├── Project.java
    │               │   └── Task.java
    │               │
    │               ├── repository
    │               │   ├── ProjectRepository.java
    │               │   └── TaskRepository.java
    │               │
    │               ├── service
    │               │   ├── ProjectService.java
    │               │   ├── ProjectServiceImpl.java
    │               │   ├── TaskService.java
    │               │   └── TaskServiceImpl.java
    │               │
    │               └── SpringappApplication.java
    │
    └── resources
        └── application.properties
```

## API ENDPOINTS
- POST - "/project" - Returns response status 201 with project object on successful creation or else 500.
- POST - "/task/project/{projectid}" - Returns response status 201 with a task object on successful mapping of the task to the projectld or else 500.
- GET - "/project/{projectld}" - Returns response status 200 with project object which includes details of task, on successful retrieval or else 404. GET-"/task" - Returns response status 200 with List<Task> object on successful retrieval or else 404.
- GET - "/task/{taskid}" - Returns response status 200 with task object on successful retrieval or else 404.
- GET - "/project/{projectid}/completed/tasks/count" - Retrieves response status 200 with the count of completed tasks associated with a specific projectld or else 404 if the specified project does not exist. The response body will contain the count as a long
value.
