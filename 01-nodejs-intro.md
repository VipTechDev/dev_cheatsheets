## 🧠 Node.js & Express Cheat Sheet  
Module 1: Introduction to Server-Side JavaScript

---

### 🌐 `http.createServer()` — Creating a Basic Server  
✅ Use the built-in `http` module to create a server that listens for client requests.

```js
const http = require('http');

const requestListener = function(req, res) {
  res.writeHead(200);
  res.end('Hello, World!');
};

const port = 8080;
const server = http.createServer(requestListener);

console.log('server listening on port: ' + port);
server.listen(port);
```

---

### 🕒 `new Date()` — Getting the Current Date  
✅ Returns a date object. You can format it or set a timezone using `toLocaleString()`.

```js
module.exports.getDate = function getDate() {
  let aestTime = new Date().toLocaleString("en-US", {
    timeZone: "Australia/Brisbane"
  });
  return aestTime;
};
```

---

### 📦 `import()` — Importing from ES Modules  
✅ Use `import` to bring in reusable logic from `.mjs` files.

```js
// addTwoNos.mjs
function addTwo(num) {
  return num + 4;
}
export { addTwo };

// app.js
import { addTwo } from './addTwoNos.mjs';

// Prints: 8
console.log(addTwo(4));
```

---

### 📥 `require()` — Importing CommonJS Modules  
✅ Use `require()` to include external modules and access their exports.

```js
// messages.js
module.exports = 'Hello Programmers';

// app.js
let msg = require('./messages.js');

console.log(msg);
```

## 🧠 JavaScript & Express Concepts Cheat Sheet  
Module 1 — Extended Fundamentals for Server-Side Development

---

### 🧮 Variable Declaration & Data Types  
✅ Use `let`, `const`, and `var` to declare variables with different scopes and mutability.

```js
let name = "Book Review";       // string
const rating = 4.5;             // number (immutable binding)
var isPublished = true;         // boolean (function-scoped)
let book = { title: "JS Guide", author: "MDN" }; // object
let tags = ["JavaScript", "Express"];            // array
```

---

### 🔁 Control Structures  
✅ Use conditionals and loops to manage logic flow.

```js
if (rating > 4) {
  console.log("Highly rated!");
} else {
  console.log("Needs improvement.");
}

for (let tag of tags) {
  console.log(tag);  // prints each tag
}
```

---

### 🧠 Functions & Arrow Syntax  
✅ Encapsulate logic with reusable functions.

```js
function greet(user) {
  return `Hello, ${user}`;
}

const add = (a, b) => a + b;

console.log(greet("Dev")); // Hello, Dev
```

---

### 📚 Array Methods — `map`, `filter`, `reduce`  
✅ Transform and process data collections.

```js
const books = [
  { title: "JS Basics", rating: 5 },
  { title: "Node Intro", rating: 3 }
];

const topBooks = books.filter(book => book.rating > 4);
const titles = books.map(book => book.title);
const averageRating = books.reduce((sum, book) => sum + book.rating, 0) / books.length;

console.log(topBooks);      // [{ title: "JS Basics", rating: 5 }]
console.log(titles);        // ["JS Basics", "Node Intro"]
console.log(averageRating); // 4
```

---

### 🧩 Object-Oriented JavaScript  
✅ Use `class` syntax to organize logic and structure.

```js
class Book {
  constructor(title, rating) {
    this.title = title;
    this.rating = rating;
  }
  describe() {
    return `${this.title} has a rating of ${this.rating}`;
  }
}

const b1 = new Book("Node Basics", 4.2);
console.log(b1.describe());
```

---

### 🔄 Working with JSON  
✅ Convert between JSON strings and JavaScript objects.

```js
let jsonData = '{"title":"Express 101","rating":5}';
const bookObj = JSON.parse(jsonData);
const newJson = JSON.stringify(bookObj);
```

---

### 🚀 Basic Express Server Setup  
✅ Create a minimal server that responds with JSON.

```js
const express = require("express");
const app = express();

app.use(express.json());

app.get("/books", (req, res) => {
  res.json([{ title: "Learn Node", rating: 4 }]);
});

app.listen(3000, () => console.log("Server running on port 3000"));
```

---

### 🌐 HTTP Methods Overview  
✅ REST verbs used for CRUD operations.

| Method | Purpose        |
|--------|----------------|
| GET    | Read data      |
| POST   | Create data    |
| PUT    | Update data    |
| DELETE | Remove data    |

---

### 📥 Accessing Request Data in Express  
✅ Use `req.params`, `req.query`, and `req.body` to extract incoming data.

```js
// req.params
app.get('/users/:id', (req, res) => {
  const userId = req.params.id;
  res.send(`User ID is ${userId}`);
});

// req.query
app.get('/books', (req, res) => {
  const author = req.query.author;
  res.send(`Filter by author: ${author}`);
});

// req.body
app.post('/register', (req, res) => {
  const username = req.body.username;
  res.send(`Username received: ${username}`);
});
```

---

## 📘 Glossary: Node.js and Express Fundamentals  
Module 1 — Introduction to Server-Side JavaScript

Welcome! This glossary complements your backend cheat sheet by defining key terms related to Node.js, Express, server architecture, and asynchronous programming. It’s alphabetized for quick lookup and designed to support modular learning and remixable workflows.

| Term               | Definition                                                                                                                                               |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Anonymous Function | A function without a name, often passed as a parameter to another function for inline execution.                                                        |
| Application Server | A server that transforms data into dynamic content and runs business logic, including data storage and transfer rules.                                  |
| Asynchronous       | A process that runs independently of others, allowing tasks like I/O operations to complete without blocking the main thread.                           |
| Callback Function  | A function passed into another function and invoked after an asynchronous task completes, enabling non-blocking behavior.                               |
| Database Server    | A dedicated server that provides database services and handles data storage, retrieval, and management.                                                  |
| Dependencies       | External code libraries or packages that are reused across modules to extend functionality.                                                              |
| Event-Driven       | A programming paradigm where the flow is determined by events like user input, server requests, or timers.                                               |
| Express.js         | A flexible web framework for Node.js that simplifies routing, middleware, and server setup.                                                              |
| Framework          | A structured platform that generates code for common tasks. Examples include Express.js, Django, and Ruby on Rails.                                     |
| HTTP Server        | Software that handles HTTP requests and responses, interpreting URLs and serving content to clients.                                                     |
| Load               | The volume of concurrent users, transactions, or data exchanged between clients and servers.                                                             |
| Module             | A file containing encapsulated JavaScript code that serves a specific purpose and can be imported elsewhere.                                             |
| Multi-Threaded     | A system where multiple tasks are executed simultaneously across different threads.                                                                      |
| Node.js            | A JavaScript runtime built on Chrome’s V8 engine, enabling server-side scripting and scalable backend development.                                      |
| Non-Blocking       | A design where one thread’s failure doesn’t affect others, and tasks don’t wait for others to finish before executing.                                   |
| Npm                | Node Package Manager — the default tool for managing packages and dependencies in Node.js projects.                                                      |
| Package            | A directory containing one or more modules bundled together for reuse.                                                                                   |
| Package.json       | A metadata file that defines a project’s dependencies, scripts, and configuration.                                                                      |
| Payload            | The actual data transmitted between client and server during a request or response.                                                                     |
| Runtime Environment| The infrastructure (hardware + software) that supports code execution. Node.js is a backend runtime environment.                                        |
| Scalability        | The ability of an application to handle increased load or shrink dynamically without degrading performance.                                              |
| Server.js          | A file that contains the logic for creating and configuring a server instance.                                                                          |
| Single-Threaded    | A system where only one task is processed at a time, typical of Node.js’s event loop model.                                                              |
| Web Server         | Software that responds to client requests, typically using HTTP to serve content or APIs.                                                               |
| Web Service        | A type of API that uses HTTP to send and receive data between clients and servers, enabling remote communication.                                       |

---

## 📘 Glossary Additions: JavaScript & Express Concepts  
Module 1 — Extended Terms for Server-Side Development

| Term               | Definition                                                                                                                                       |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| Arrow Function      | A concise syntax for writing functions using `=>`, often used for inline callbacks and cleaner logic.                                           |
| Array Method        | Built-in functions like `map`, `filter`, and `reduce` used to transform or process arrays.                                                      |
| Class               | A blueprint for creating objects with shared structure and behavior using `constructor` and methods.                                            |
| Control Structure   | Constructs like `if`, `else`, and `for` that manage the flow of logic in a program.                                                             |
| JSON                | JavaScript Object Notation — a lightweight format for data exchange between client and server.                                                  |
| JSON.parse()        | Converts a JSON string into a JavaScript object.                                                                                                |
| JSON.stringify()    | Converts a JavaScript object into a JSON string.                                                                                                |
| req.body            | An Express object that holds data sent in the body of a POST request, typically in JSON format.                                                |
| req.params          | An Express object that holds route parameters defined in the URL path (e.g. `/users/:id`).                                                      |
| req.query           | An Express object that holds query string parameters from the URL (e.g. `/books?author=John`).                                                  |
| REST Methods        | HTTP verbs (`GET`, `POST`, `PUT`, `DELETE`) used to perform CRUD operations in web services.                                                    |
| Variable Declaration| The use of `let`, `const`, or `var` to define variables with different scopes and mutability.                                                   |
