Here’s a cheat sheet for APIs and RESTful Services, covering key principles and methods (GET, POST, etc.) in Markdown format.

````markdown
# APIs & RESTful Services Cheat Sheet

## What is a REST API?

A **REST (Representational State Transfer)** API is an architectural style for
building web services that allow systems to communicate over HTTP. It relies on
stateless communication and standard HTTP methods to perform operations on resources.

## Key Principles of REST

1. **Client-Server Architecture**: Separation of client and server responsibilities.
2. **Statelessness**: Each request from the client must contain all the information the server needs to fulfill the request.
3. **Cacheability**: Responses from the server can be cached to improve performance.
4. **Uniform Interface**: A consistent and standard way to communicate with the server, often using URIs to represent resources.
5. **Layered System**: REST allows intermediaries like load balancers or proxies between the client and the server.
6. **Code on Demand (optional)**: Servers can extend functionality by sending executable code to the client.

## Common HTTP Methods in RESTful APIs

### 1. GET

- **Purpose**: Retrieve data from the server.
- **Use Case**: Fetching a resource or a list of resources.
- **Example**:
  ```http
  GET /api/users
  ```
````

**Response** (200 OK):

```json
[
  {
    "id": 1,
    "name": "John Doe"
  },
  {
    "id": 2,
    "name": "Jane Doe"
  }
]
```

### 2. POST

- **Purpose**: Send data to the server to create a new resource.
- **Use Case**: Submitting a form or creating a new user.
- **Example**:

  ```http
  POST /api/users
  Content-Type: application/json

  {
    "name": "John Doe",
    "email": "john@example.com"
  }
  ```

  **Response** (201 Created):

  ```json
  {
    "id": 3,
    "name": "John Doe",
    "email": "john@example.com"
  }
  ```

### 3. PUT

- **Purpose**: Update an existing resource entirely.
- **Use Case**: Replacing an entire resource or user data.
- **Example**:

  ```http
  PUT /api/users/1
  Content-Type: application/json

  {
    "name": "John Smith",
    "email": "johnsmith@example.com"
  }
  ```

  **Response** (200 OK):

  ```json
  {
    "id": 1,
    "name": "John Smith",
    "email": "johnsmith@example.com"
  }
  ```

### 4. PATCH

- **Purpose**: Partially update an existing resource.
- **Use Case**: Modifying specific fields of a resource.
- **Example**:

  ```http
  PATCH /api/users/1
  Content-Type: application/json

  {
    "email": "johnnew@example.com"
  }
  ```

  **Response** (200 OK):

  ```json
  {
    "id": 1,
    "name": "John Doe",
    "email": "johnnew@example.com"
  }
  ```

### 5. DELETE

- **Purpose**: Delete a resource from the server.
- **Use Case**: Removing a user or data.
- **Example**:

  ```http
  DELETE /api/users/1
  ```

  **Response** (204 No Content):

  - No body is returned.

## HTTP Status Codes in REST APIs

- **200 OK**: The request was successful.
- **201 Created**: A new resource was created.
- **204 No Content**: The request was successful, but no content is returned.
- **400 Bad Request**: The server could not understand the request due to invalid syntax.
- **401 Unauthorized**: Authentication is required.
- **403 Forbidden**: The client does not have permission to access the resource.
- **404 Not Found**: The requested resource could not be found.
- **500 Internal Server Error**: The server encountered an error and could not complete the request.

## RESTful Resource Naming Conventions

- **Resources should be nouns**: Use nouns to describe the resources in URIs, not verbs.

  - Example: `/api/users`, `/api/posts`.

- **Use plural nouns**: It is common to use plural nouns to represent collections.

  - Example: `/api/users` refers to a collection of users.

- **Use hierarchy in URLs**: Show relationships between resources.
  - Example: `/api/users/1/posts` to represent posts belonging to a user.

## Request Headers

- **Content-Type**: Specifies the type of data being sent (e.g., `application/json`).
- **Authorization**: Used for authentication, often containing a token (e.g., `Bearer <token>`).
- **Accept**: Tells the server what kind of response the client expects (e.g., `application/json`).

## Example Workflow: CRUD Operations on a User

### 1. Create a New User (POST)

```http
POST /api/users
Content-Type: application/json

{
  "name": "John Doe",
  "email": "john@example.com"
}
```

### 2. Retrieve All Users (GET)

```http
GET /api/users
```

### 3. Retrieve a Single User by ID (GET)

```http
GET /api/users/1
```

### 4. Update a User (PUT)

```http
PUT /api/users/1
Content-Type: application/json

{
  "name": "John Smith",
  "email": "johnsmith@example.com"
}
```

### 5. Delete a User (DELETE)

```http
DELETE /api/users/1
```

## RESTful vs Non-RESTful Services

- **RESTful**: Follows the principles of REST and uses standard HTTP methods for CRUD operations.
- **Non-RESTful**: May use different protocols or methods (e.g., SOAP, XML-RPC) for communication.

---

This cheat sheet provides a concise overview of the core concepts for building and interacting with RESTful APIs.

This covers the fundamental aspects of RESTful services and common HTTP methods.
