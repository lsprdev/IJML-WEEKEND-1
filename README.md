# Hackathon IJML(It's Just Myself, Literally) - Weekend 1

Welcome to my hackathon project! This is a project for the first weekend of Hackathon IJML. The goal is to create a RESTful API using Django Rest Framework and a simple front-end interface using Vue.js. And yeah, I'm the only participant in this hackathon, so it's just myself, literally.

Feel free to join me if you want to — just clone this repo, delete my code, and have fun! 🚀

### Challenge Overview

The challenge is to create a RESTful API using Django Rest Framework and a simple front-end interface using Vue.js. The API should have CRUD operations for users, an endpoint for login, and authentication for the endpoints.

### Requirements:

- Develop CRUD for users (Create, List, Update, and Delete).
- Develop an endpoint for login.
- The user schema must contain the following fields: Name, Age, Email, Password, and User Types. Possible user types are ADMIN and CLIENT.
- Develop the process of authentication for the endpoints(Use JWT). Only the user registration and login endpoints should be public, the other endpoints should be protected.
- Document the endpoints (Postman or Insomnia) how to export, and add them to the project.
- Use PostgreSQL as the database.
- Use Docker to containerize the application.
- Develop a simple front-end interface using Vue.js to interact with the API.
- Add instructions on how to run the project.

### Must Have Endpoints:

- POST /signup
- POST /login
- GET /users
- POST /users
- PUT /users/:id
- DELETE /users/:id

### Payload:

Propose a payload you like. If you prefer, here are some examples:

GET /users

```json
{
    "message": "Users listed successfully!",
    "data": 
    [{
        "name": "Gabriel",
        "age": 19,
        "email": "gabriel@lspr.dev",
        "password": "162677a7c6abd2f3d37168b3",
        "isAdmin": false
    },
    {
        "name": "Admin",
        "age": null,
        "email": "admin@admin.com",
        "password": "429667a7u6cyd2f3d37112j8",
        "isAdmin": true
    }]
}
```
POST /users

```json
{
  "name": "Gabriel",
  "age": 19,
  "email": "gabriel@lspr.dev",
  "password": "qwerty123",
  "isAdmin": false
}
```

### Useful Materials

- https://www.django-rest-framework.org/
- https://www.django-rest-framework.org/api-guide/authentication/
- https://docs.docker.com/samples/django/
- https://vuejs.org/
- https://www.postman.com/
- https://docs.insomnia.rest/insomnia/import-export-data

LET'S GOOO! 🏆 🏆