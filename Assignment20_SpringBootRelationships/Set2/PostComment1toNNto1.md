# Post and Comment One-to-Many Many-to-One Mapping

## Overview:
Create a Spring Boot application with two entities: "Post" and "Comment". A post can have multiple comments, and a comment can belong to only one post. Implement a one-to-many bidirectional mapping between these entities using Spring JPA. 

## Functional Requirements:
Create folders named controller, model, repository, and service inside the **postcomment1tonnto1/src/main/java/com/giftabled/postcomment1tonnto1**.

Inside the controller folder, create classes named "PostController" and "CommentController".

Inside the model folder, Create a class named "Post" with the following attributes:
1. id - int(auto-generated primary key)
2. title - String
3. content - String
4. comments - List<Comment> (OneToMany, mappedBy="post", JsonManagedReference)

Create another class named "Comment" with the following attributes:
1. id - int(auto-generated primary key)
2. text - String
3. post - Post (ManyToOne, JsonBackReference)

Implement getters, setters, and constructors for the Team and Player entities.

Inside the repository folder, create interfaces named "PostRepo" and "CommentRepo".

Inside the service folder, create interfaces named "PostService" and "CommentService".

Also, create classes PostServiceImpl and CommentServiceImpl and it should implement the PostService and CommentService.

## Project Structure
Refer to the below image for the project structure:

```text
└── src
    └── main
        ├── java
        │   └── com
        │       └── giftabled
        │           └── postcomment1tonnto1
        │               ├── controller
        │               │   ├── CommentController.java
        │               │   └── PostController.java
        │               │
        │               ├── model
        │               │   ├── Comment.java
        │               │   └── Post.java
        │               │
        │               ├── repository
        │               │   ├── CommentRepo.java
        │               │   └── PostRepo.java
        │               │
        │               ├── service
        │               │   ├── CommentService.java
        │               │   ├── CommentServiceImpl.java
        │               │   ├── PostService.java
        │               │   └── PostServiceImpl.java
        │               │
        │               └── SpringappApplication.java
        │
        └── resources
            └── application.properties
```

## API ENDPOINTS
- POST - "/post" - Returns response status 201 with post object on successful creation or else 500.
- POST - "/comment/post/{postid}" - Returns response status 201 with a comment object on successfully mapping the comment to the postid or else 500.
- GET - "/post/{postid}" - Returns response status 200 with post object, which includes details of comment on successful retrieval or else 404.
- PUT - "/comment/{commentid}" - Returns response status 200 with updated comment object on successful updation or else 404.
- DELETE - "/comment/{commentId} - Returns response status 200 with String "Comment deleted successfully" on successful deletion or else "Comment not found with ID " + commentld.
