Here's your **Node.js Cheat Sheet** formatted in Markdown, maintaining the same clear structure as before:

````markdown
# Node.js Cheat Sheet

## File System Operations

### Importing the File System Module

```javascript
const fs = require('fs');
```
````

### Reading Files

- **Asynchronous**:

  ```javascript
  fs.readFile('file.txt', 'utf8', (err, data) => {
      if (err) throw err;
      console.log(data);
  });
  ```

- **Synchronous**:
  ```javascript
  const data = fs.readFileSync('file.txt', 'utf8');
  console.log(data);
  ```

### Writing Files

- **Asynchronous**:

  ```javascript
  fs.writeFile('file.txt', 'Hello, world!', (err) => {
      if (err) throw err;
      console.log('File has been saved!');
  });
  ```

- **Synchronous**:
  ```javascript
  fs.writeFileSync('file.txt', 'Hello, world!');
  console.log('File has been saved!');
  ```

### Appending to Files

- **Asynchronous**:

  ```javascript
  fs.appendFile('file.txt', 'Appended text.', (err) => {
      if (err) throw err;
      console.log('Text has been appended!');
  });
  ```

- **Synchronous**:
  ```javascript
  fs.appendFileSync('file.txt', 'Appended text.');
  console.log('Text has been appended!');
  ```

### Deleting Files

```javascript
fs.unlink('file.txt', (err) => {
    if (err) throw err;
    console.log('File deleted!');
});
```

### Creating Directories

- **Asynchronous**:

  ```javascript
  fs.mkdir('newDirectory', (err) => {
      if (err) throw err;
      console.log('Directory created!');
  });
  ```

- **Synchronous**:
  ```javascript
  fs.mkdirSync('newDirectory');
  console.log('Directory created!');
  ```

---

## Modules

### Creating a Module

```javascript
// myModule.js
const myFunction = () => {
    console.log('Hello from my module!');
};

module.exports = myFunction;
```

### Importing a Module

```javascript
const myFunction = require('./myModule');
myFunction(); // Output: Hello from my module!
```

### Using Built-in Modules

- **Path**:

  ```javascript
  const path = require('path');
  const filePath = path.join(__dirname, 'file.txt');
  ```

- **HTTP**:
  ```javascript
  const http = require('http');
  ```

---

## HTTP Requests

### Creating a Simple Server

```javascript
const http = require('http');

const server = http.createServer((req, res) => {
    res.statusCode = 200;
    res.setHeader('Content-Type', 'text/plain');
    res.end('Hello, World!\n');
});

server.listen(3000, () => {
    console.log('Server running at http://localhost:3000/');
});
```

### Making HTTP Requests (Using `axios`)

```javascript
const axios = require('axios');

axios.get('https://jsonplaceholder.typicode.com/posts')
    .then(response => {
        console.log(response.data);
    })
    .catch(error => {
        console.error(error);
    });
```

---

## Middleware (Using Express)

### Setting Up Express

```javascript
const express = require('express');
const app = express();
const port = 3000;
```

### Middleware Example

```javascript
app.use(express.json()); // Parses JSON bodies

app.use((req, res, next) => {
    console.log(`${req.method} ${req.url}`);
    next(); // Passes control to the next middleware
});
```

### Defining Routes

```javascript
app.get('/', (req, res) => {
    res.send('Hello, World!');
});

app.post('/data', (req, res) => {
    console.log(req.body);
    res.send('Data received');
});
```

### Starting the Server

```javascript
app.listen(port, () => {
    console.log(`Server running at http://localhost:${port}/`);
});
```

---

This cheat sheet provides a quick reference for common Node.js operations, including file system interactions, module usage, HTTP requests, and Express middleware.

```

Let me know if you need any further changes or additional cheat sheets!
```
