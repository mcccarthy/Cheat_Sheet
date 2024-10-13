# Node.js Cheat Sheet

## 1. **Node.js Setup**

| Concept               | Description                                     | Code Example                                              |
|-----------------------|-------------------------------------------------|-----------------------------------------------------------|
| **Install Node.js**    | Install Node.js on your machine via package manager. | ```bash npm install -g node ``` |
| **Check Version**     | Verify Node.js and npm versions installed.      | ```bash node -v && npm -v ``` |
| **Initialize a Project** | Create a new `package.json` file for a Node.js project. | ```bash npm init ``` |
| **Install Dependencies** | Install third-party packages using npm.        | ```bash npm install express ``` |
| **Run a Script**      | Use the `node` command to run a JavaScript file. | ```bash node app.js ``` |

---

## 2. **Node.js Modules**

| Concept               | Description                                     | Code Example                                              |
|-----------------------|-------------------------------------------------|-----------------------------------------------------------|
| **Built-in Modules**  | Node.js comes with core modules like `fs`, `http`, `path`, etc. | ```javascript const fs = require('fs'); const http = require('http'); ``` |
| **Create a Module**   | Export and import your own modules.             | ```javascript // math.js module.exports.add = (a, b) => a + b; ``` ```javascript // app.js const math = require('./math'); console.log(math.add(2, 3)); ``` |
| **ES6 Imports**       | Use ES6 `import/export` in modules (requires enabling module support). | ```javascript import { add } from './math.mjs'; ``` |

---

## 3. **File System (fs) Module**

| Concept               | Description                                     | Code Example                                              |
|-----------------------|-------------------------------------------------|-----------------------------------------------------------|
| **Read File (Async)** | Read a file asynchronously.                     | ```javascript const fs = require('fs'); fs.readFile('file.txt', 'utf8', (err, data) => { if (err) throw err; console.log(data); }); ``` |
| **Write File (Async)** | Write data to a file asynchronously.           | ```javascript fs.writeFile('file.txt', 'Hello, Node.js!', (err) => { if (err) throw err; console.log('File written'); }); ``` |
| **Delete File**       | Delete a file using `fs.unlink()`.              | ```javascript fs.unlink('file.txt', (err) => { if (err) throw err; console.log('File deleted'); }); ``` |

---

## 4. **HTTP Server**

| Concept               | Description                                     | Code Example                                              |
|-----------------------|-------------------------------------------------|-----------------------------------------------------------|
| **Create Server**     | Set up a basic HTTP server in Node.js.          | ```javascript const http = require('http'); const server = http.createServer((req, res) => { res.statusCode = 200; res.setHeader('Content-Type', 'text/plain'); res.end('Hello, World!\n'); }); server.listen(3000, () => { console.log('Server running at http://localhost:3000/'); }); ``` |
| **Handle Routing**    | Handle basic routes manually.                   | ```javascript if (req.url === '/about') { res.end('About Page'); } else { res.end('Home Page'); } ``` |

---

## 5. **Express.js Framework**

| Concept               | Description                                     | Code Example                                              |
|-----------------------|-------------------------------------------------|-----------------------------------------------------------|
| **Install Express**   | Install the Express.js package.                 | ```bash npm install express ``` |
| **Basic Express Server** | Set up a simple web server using Express.      | ```javascript const express = require('express'); const app = express(); app.get('/', (req, res) => { res.send('Hello, Express!'); }); app.listen(3000, () => { console.log('Server running on port 3000'); }); ``` |
| **Middleware**        | Add middleware for request processing.          | ```javascript app.use((req, res, next) => { console.log('Middleware running'); next(); }); ``` |
| **Serving Static Files** | Serve static files like HTML, CSS, and images. | ```javascript app.use(express.static('public')); ``` |
| **Handling Routes**   | Define route handlers for different HTTP methods. | ```javascript app.get('/user', (req, res) => { res.send('GET user'); }); app.post('/user', (req, res) => { res.send('POST user'); }); ``` |

---

## 6. **Environment Variables**

| Concept               | Description                                     | Code Example                                              |
|-----------------------|-------------------------------------------------|-----------------------------------------------------------|
| **Set Environment Variables** | Use `process.env` to access environment variables. | ```bash export PORT=3000 ``` ```javascript const port = process.env.PORT || 3000; app.listen(port); ``` |
| **dotenv Package**    | Load environment variables from a `.env` file.  | ```bash npm install dotenv ``` ```javascript require('dotenv').config(); const port = process.env.PORT; ``` |

---

## 7. **Asynchronous JavaScript**

| Concept               | Description                                     | Code Example                                              |
|-----------------------|-------------------------------------------------|-----------------------------------------------------------|
| **Promises**          | Handle asynchronous operations using promises.  | ```javascript const fetchData = () => new Promise((resolve, reject) => { setTimeout(() => resolve('Data fetched'), 2000); }); fetchData().then(data => console.log(data)); ``` |
| **Async/Await**       | Simplify async code using `async`/`await`.      | ```javascript async function getData() { const data = await fetchData(); console.log(data); } getData(); ``` |
| **Handle Errors**     | Use `try/catch` to handle async errors.         | ```javascript try { const data = await fetchData(); } catch (error) { console.log('Error:', error); } ``` |

---

## 8. **Database Integration (MongoDB)**

| Concept               | Description                                     | Code Example                                              |
|-----------------------|-------------------------------------------------|-----------------------------------------------------------|
| **Install Mongoose**  | Install Mongoose ODM for MongoDB.               | ```bash npm install mongoose ``` |
| **Connect to Database** | Establish a connection to a MongoDB database.   | ```javascript const mongoose = require('mongoose'); mongoose.connect('mongodb://localhost:27017/mydb', { useNewUrlParser: true, useUnifiedTopology: true }); ``` |
| **Define a Schema**   | Define a schema for a MongoDB collection.       | ```javascript const userSchema = new mongoose.Schema({ name: String, age: Number }); const User = mongoose.model('User', userSchema); ``` |
| **CRUD Operations**   | Perform Create, Read, Update, Delete operations. | ```javascript // Create const newUser = new User({ name: 'John', age: 30 }); newUser.save(); // Read User.find({}, (err, users) => console.log(users)); ``` |

---

## 9. **Error Handling**

| Concept               | Description                                     | Code Example                                              |
|-----------------------|-------------------------------------------------|-----------------------------------------------------------|
| **try/catch Block**   | Use `try/catch` for error handling in async/await. | ```javascript try { const data = await fetchData(); } catch (err) { console.log('Error:', err); } ``` |
| **Global Error Handling Middleware** | Handle errors globally in Express.js. | ```javascript app.use((err, req, res, next) => { console.error(err.stack); res.status(500).send('Something broke!'); }); ``` |

---

## 10. **Node.js Best Practices**

| Concept               | Description                                     |
|-----------------------|-------------------------------------------------|
| **Modular Code**      | Keep your code modular by splitting files into smaller modules. |
| **Environment Config** | Store environment variables securely using `.env` files or services like AWS Secrets Manager. |
| **Security**          | Use middleware like `helmet` for HTTP headers, and always sanitize inputs. |
| **Error Handling**    | Implement consistent error handling across routes and async functions. |
| **Logging**           | Use a proper logging system like `winston` or `morgan`. |
| **Testing**           | Write unit tests using frameworks like `Jest` or `Mocha`. |

---

This **Node.js Cheat Sheet** covers fundamental concepts for setting up a Node.js server, handling routes, middleware, and interacting with databases. It also touches on async/await, error handling, and best practices.


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