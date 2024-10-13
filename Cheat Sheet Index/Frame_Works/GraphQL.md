# GraphQL Cheat Sheet

## 1. **Core Concepts**

| Concept                  | Description                                      | Example |
|--------------------------|--------------------------------------------------|---------|
| **Schema**                | Defines the types, queries, and mutations available in the API. | ```graphql type Query { books: [Book] } ``` |
| **Query**                 | A read-only request to retrieve data from the API. | ```graphql { books { title author } } ``` |
| **Mutation**              | A write request to modify data on the server.   | ```graphql mutation { addBook(title: "New Book", author: "Author Name") { id } } ``` |
| **Type**                  | Defines the shape of data (like models).        | ```graphql type Book { id: ID! title: String! author: String! } ``` |
| **Resolver**              | A function that resolves a query or mutation to return the data. | ```javascript const resolvers = { Query: { books: () => getBooks() } }; ``` |
| **Scalar Types**          | Basic data types: `Int`, `Float`, `String`, `Boolean`, `ID`. | ```graphql type Book { title: String! pages: Int } ``` |

---

## 2. **Query Syntax**

| Concept                  | Description                                      | Example |
|--------------------------|--------------------------------------------------|---------|
| **Simple Query**          | Request specific fields from an object.          | ```graphql { book(id: 1) { title author } } ``` |
| **Nested Query**          | Retrieve related data by nesting fields.         | ```graphql { book(id: 1) { title author reviews { rating comment } } } ``` |
| **Arguments**             | Pass arguments to a query to filter results.     | ```graphql { books(genre: "Fiction") { title } } ``` |
| **Aliases**               | Rename fields in the query result.               | ```graphql { book: book(id: 1) { title author } } ``` |
| **Fragments**             | Reuse field selections across multiple queries.  | ```graphql fragment BookFields on Book { title author } query { book(id: 1) { ...BookFields } } ``` |

---

## 3. **Mutations**

| Concept                  | Description                                      | Example |
|--------------------------|--------------------------------------------------|---------|
| **Basic Mutation**        | Modify data on the server (insert, update, delete). | ```graphql mutation { addBook(title: "New Book", author: "Author") { id title } } ``` |
| **Input Types**           | Use input types to pass complex objects as arguments. | ```graphql input BookInput { title: String! author: String! } mutation { addBook(input: { title: "Book", author: "Author" }) { id } } ``` |
| **Multiple Mutations**    | Run multiple mutations in a single request.      | ```graphql mutation { addAuthor(name: "Author") { id } addBook(title: "Book", authorId: 1) { id } } ``` |

---

## 4. **Subscriptions**

| Concept                  | Description                                      | Example |
|--------------------------|--------------------------------------------------|---------|
| **Basic Subscription**    | Real-time updates when data changes.             | ```graphql subscription { bookAdded { id title } } ``` |
| **Subscription with Arguments** | Receive updates with filtering criteria. | ```graphql subscription { bookAdded(genre: "Sci-Fi") { title } } ``` |

---

## 5. **Directives**

| Concept                  | Description                                      | Example |
|--------------------------|--------------------------------------------------|---------|
| **@include**              | Conditionally include fields based on variables. | ```graphql query getBook($includeAuthor: Boolean!) { book(id: 1) { title author @include(if: $includeAuthor) } } ``` |
| **@skip**                 | Conditionally skip fields.                      | ```graphql query getBook($skipAuthor: Boolean!) { book(id: 1) { title author @skip(if: $skipAuthor) } } ``` |

---

## 6. **GraphQL Variables**

| Concept                  | Description                                      | Example |
|--------------------------|--------------------------------------------------|---------|
| **Using Variables**       | Pass variables into a query.                    | ```graphql query getBook($id: ID!) { book(id: $id) { title author } } ``` |
| **Variable Definitions**  | Define variables with types in a query.          | ```graphql query getBook($id: ID!) { book(id: $id) { title } } ``` |
| **Mutation with Variables** | Use variables in mutations.                   | ```graphql mutation addBook($title: String!, $author: String!) { addBook(title: $title, author: $author) { id } } ``` |

---

## 7. **Error Handling**

| Concept                  | Description                                      | Example |
|--------------------------|--------------------------------------------------|---------|
| **Errors in Queries**     | Handle errors in query responses.                | ```json { "errors": [ { "message": "Book not found" } ] } ``` |
| **Custom Errors**         | Define custom errors in resolvers.               | ```javascript throw new Error("Custom error message"); ``` |

---

## 8. **Authentication**

| Concept                  | Description                                      | Example |
|--------------------------|--------------------------------------------------|---------|
| **Authorization Headers** | Pass auth tokens in the request headers.         | ```bash curl -H "Authorization: Bearer <token>" -X POST -d '{ "query": "{ user { id name } }" }' http://localhost:4000/graphql ``` |
| **Securing Resolvers**    | Add authentication logic in resolvers.           | ```javascript const resolvers = { Query: { user: (parent, args, context) => { if (!context.user) throw new Error('Not authenticated'); return getUser(context.user.id); } } }; ``` |

---

## 9. **Pagination**

| Concept                  | Description                                      | Example |
|--------------------------|--------------------------------------------------|---------|
| **Cursor-based Pagination** | Use cursors to paginate through data.          | ```graphql query { books(first: 10, after: "cursor") { edges { node { title } cursor } pageInfo { hasNextPage endCursor } } } ``` |
| **Offset-based Pagination** | Use offsets to skip over data.                 | ```graphql query { books(offset: 0, limit: 10) { title author } } ``` |

---

## 10. **GraphQL Best Practices**

- **Modular Schemas**: Split schemas into smaller parts for better organization.
- **Batched Queries**: Request multiple fields in one query to reduce network overhead.
- **Avoid Over-fetching**: Only request the necessary fields to optimize performance.

---

This **GraphQL Cheat Sheet** provides a comprehensive overview of key concepts like queries, mutations, subscriptions, schema design, and best practices for API development with GraphQL.


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