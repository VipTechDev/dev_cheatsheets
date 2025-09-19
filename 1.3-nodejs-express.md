# 🚀 Express.js Cheat Sheet  
Module 3: Web Application Framework

---

## 📦 `package.json` — Declaring Express Dependency  
✅ To use Express version 4.x, declare it like this:

```json
"dependencies": {
  "express": "4.x"
}
```

---

## 🆕 `new express()` — Create Express App  
✅ Initializes an Express server instance.

```js
const express = require("express");
const app = new express();
```

---

## 🎧 `app.listen()` — Start Server  
✅ Binds and listens for connections on the specified port.

```js
app.listen(3333, () => {
  console.log("Listening at http://localhost:3333");
});
```

---

## 📥 `app.get()` — Handle GET Requests  
✅ Responds to GET requests at a specific endpoint.

```js
// handles GET queries to endpoint /user/about/:id
app.get("/user/about/:id", (req, res) => {
  res.send("Response about user " + req.params.id);
});
```

---

## 📝 `app.post()` — Handle POST Requests  
✅ Responds to POST requests at a specific endpoint.

```js
// handles POST queries to endpoint /user/about/:id
app.post("/user/about/:id", (req, res) => {
  res.send("Response about user " + req.params.id);
});
```

---

## 🛡️ `app.use()` — Middleware Setup  
✅ Middleware runs before route handlers and can modify the request/response.

```js
const express = require("express");
const app = new express();

function myLogger(req, res, next) {
  req.timeReceived = Date();
  next();
}

app.use(myLogger);

app.get("/", (req, res) => {
  res.send("Request received at " + req.timeReceived + " is a success!");
});
```

---

## 🧭 `express.Router()` — Router-Level Middleware  
✅ Use routers to modularize middleware and route logic.

```js
const express = require("express");
const app = new express();

let userRouter = express.Router();
let itemRouter = express.Router();

userRouter.use((req, res, next) => {
  console.log("User query time:", Date());
  next();
});

userRouter.get("/:id", (req, res) => {
  res.send("User " + req.params.id + " last successful login " + Date());
});

app.use("/user", userRouter);

app.listen(3333, () => {
  console.log("Listening at http://localhost:3333");
});
```

---

## 🖼️ `express.static()` — Serve Static Files  
✅ Serves static HTML, images, and other assets.

```js
const express = require("express");
const app = new express();

app.use(express.static("cad220_staticfiles"));

app.listen(3333, () => {
  console.log("Listening at http://localhost:3333");
});
```

---

## 🔐 `jsonwebtoken.sign()` — Create JWT  
✅ Signs a payload to generate a JSON Web Token.

```js
if (uname === "user" && pwd === "password") {
  return res.json({
    token: jsonwebtoken.sign({ user: "user" }, JWT_SECRET),
  });
}
```

---

## ✅ `jsonwebtoken.verify()` — Verify JWT  
✅ Verifies a token using the secret key.

```js
const verificationStatus = jsonwebtoken.verify(tokenValue, "aVeryVerySecretString");
```

---

## 🗂️ Project Structure — Recommended Layout  
✅ A modular folder structure for Express APIs.

```
test-project/
  node_modules/
  config/
    db.js           // Database connection and config
    credentials.js  // API keys and secrets
  models/           // Mongoose schemas
    items.js
    prices.js
  routes/           // Route handlers
    items.js
    prices.js
  app.js
  routes.js         // Aggregate all routes here
  package.json
```

---
