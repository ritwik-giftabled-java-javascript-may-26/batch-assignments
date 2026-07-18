# User and Posts One-to-Many Many-to-One Mapping

## Overview:
Create a Spring Boot application with two entities: "User" and "Post". A user can have multiple posts.. Implement a one-to-many bidirectional mapping between these entities using Spring JPA. 

## Functional Requirements:
Create folders named controller, model, repository, and service inside the userposts1tonnto1/src/main/java/com/giftabled/userposts1tonnto1.

Inside the controller folder, create classes named "UserController" and "PostController".

Inside the model folder, Create a class named "User" with the following attributes:
1. userld - int(auto-generated, primary key)
2. username -String
3. email - String
4. posts - List<Post>(OneToMany, mapped By = "user", Json ManagedReference)

Create another class named "Post" with the following attributes:
1. postid- int(auto-generated, primary key)
2. title - String
3. content - String
4. user - User (ManyToOne, JsonBackReference)

Implement getters, setters, and constructors for the User and Post entities.

Inside the repository folder, create interfaces named "UserRepository" and "PostRepository".

Inside the service folder, create interfaces named "UserService" and "PostService".

Also, create classes UserServicelmpl and PostServiceImpl and they should implement the UserService and PostService.

## Project Structure
Refer to the below image for the project structure:

```text
src
└── main
    ├── java
    │   └── com
    │       └── giftabled
    │           └── userposts1tonnto1
    │               ├── controller
    │               │   ├── PostController.java
    │               │   └── UserController.java
    │               │
    │               ├── model
    │               │   ├── Post.java
    │               │   └── User.java
    │               │
    │               ├── repository
    │               │   ├── PostRepository.java
    │               │   └── UserRepository.java
    │               │
    │               ├── service
    │               │   ├── PostService.java
    │               │   ├── PostServiceImpl.java
    │               │   ├── UserService.java
    │               │   └── UserServiceImpl.java
    │               │
    │               └── SpringappApplication.java
    │
    └── resources
        └── application.properties
```

## API ENDPOINTS
- POST - "/user" - Returns response status 201 with user object on successful creation or else 500.
- POST - "/post/user/{userid}" - Returns response status 201 with a post object on successfully mapping of the post to the userld or else 500.
- GET - "/user/{userid}" - Returns response status 200 with user object which includes details of post, on successful retrieval or else 404.
- GET - "/post" - Returns response status 200 with List<Post> object on successful retrieval or else 404.
- GET - "/post/{postid}" - Returns response status 200 with post object on successful retrieval or else 404.
- PUT - "/post/{postid}" - Returns response status 200 with the updated post object on successful updation, or else 404. The fields tiltle and content of the post are modifiable. 
- DELETE - "/post/{postid}" - Returns response status 200 with String "Post deleted successfully" on successful deletion or else "Post not found with ID: " + postld.
