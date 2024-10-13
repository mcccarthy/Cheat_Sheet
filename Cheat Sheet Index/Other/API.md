# API Cheat Sheet

## RESTful API Principles

| Principle                 | Description                                         |
|---------------------------|-----------------------------------------------------|
| **Stateless**             | Each request from the client contains all the information needed to process it. The server does not store any session information. |
| **Client-Server Architecture** | The client and server are separate entities, allowing for independent development and scalability. |
| **Uniform Interface**     | A standardized way of interacting with the API using consistent conventions. |
| **Resource-Based**        | APIs should expose resources (e.g., users, products) that can be accessed through URIs. |
| **HTTP Methods**          | Standard methods (GET, POST, PUT, DELETE) define operations on resources. |
| **Representation**        | Resources are represented in various formats (e.g., JSON, XML) to facilitate communication. |
| **Cacheable**             | Responses should define themselves as cacheable or not, improving efficiency. |

* * *

## Common HTTP Methods

| Method      | Description                                         | Safe | Idempotent |
|-------------|-----------------------------------------------------|------|------------|
| **GET**     | Retrieve data from the server.                     | Yes  | Yes        |
| **POST**    | Submit data to the server (e.g., create a resource). | No   | No         |
| **PUT**     | Update a resource or create it if it doesn't exist. | No   | Yes        |
| **DELETE**  | Remove a resource from the server.                 | No   | Yes        |
| **PATCH**   | Partially update a resource.                        | No   | Yes        |

* * *

## Authentication Methods

| Method           | Description                                         |
|------------------|-----------------------------------------------------|
| **API Keys**     | A unique key that identifies the client, often passed in the header or query string. |
| **Basic Auth**   | Encodes username and password in Base64 and sends them in the Authorization header. |
| **Bearer Token** | A token-based authentication where the client sends a token in the Authorization header. |
| **OAuth**        | A secure authentication protocol that allows users to grant access to their resources without sharing credentials, typically using access tokens. |
| **JWT (JSON Web Token)** | A compact, URL-safe means of representing claims to be transferred between two parties, allowing for stateless authentication. |

* * *

## API Response Codes

| Status Code | Description                                         |
|-------------|-----------------------------------------------------|
| **200 OK**  | The request was successful.                         |
| **201 Created** | The resource was successfully created.           |
| **204 No Content** | The request was successful, but there's no content to return. |
| **400 Bad Request** | The server could not understand the request due to invalid syntax. |
| **401 Unauthorized** | Authentication is required and has failed or not been provided. |
| **403 Forbidden** | The server understands the request, but it refuses to authorize it. |
| **404 Not Found** | The requested resource could not be found.       |
| **500 Internal Server Error** | A generic error message indicating that the server encountered an unexpected condition. |

---

This cheat sheet provides an overview of key concepts and methods used in RESTful APIs, making it a useful reference for developers working with APIs.


Key Command
Ctrl/Cmd + B Toggle bold
Ctrl/Cmd + I Toggle italic
Alt+S (on Windows) Toggle strikethrough1
Ctrl + Shift + ] Toggle heading (uplevel)
Ctrl + Shift + [ Toggle heading (downlevel)
Ctrl/Cmd + M Toggle math environment
Alt + C Check/Uncheck task list item
Ctrl/Cmd + Shift + V Toggle preview
Ctrl/Cmd + K V Toggle preview to side