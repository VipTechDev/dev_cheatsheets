# 🧠 Node.js & Express Cheat Sheet  
Module 2: Asynchronous I/O with Callback Programming

---

## ⏳ `async/await` — Handling Promises in Async Functions  
✅ Use `await` inside `async` functions to pause execution until a promise resolves.

```js
const axios = require('axios').default;
const url = "https://example.com/data";

async function asyncCall() {
  console.log('Calling...');
  const result = await axios.get(url);
  console.log(result.data);
}

asyncCall();
```

---

## 🔁 `callback` — Passing Functions as Arguments  
✅ A callback is a function passed into another function and executed after a task completes.

```js
axios.get(url)
  .then(function(res) {
    console.log(res);
  })
  .catch(function(err) {
    console.log(err);
  });
```

---

## 📦 `Promise` — Managing Asynchronous Results  
✅ A promise represents a future value. It can be pending, fulfilled, or rejected.

```js
axios.get(url)
  .then(response => {
    // handle success
  })
  .catch(error => {
    // handle error
  });
```

---

## 📁 `Promise` Use Case — Reading Files Asynchronously  
✅ Promises are ideal for tasks like I/O operations or remote requests.

```js
const prompt = require('prompt-sync')();
const fs = require('fs');

const methCall = new Promise((resolve, reject) => {
  let filename = prompt('Enter filename: ');
  try {
    const data = fs.readFileSync(filename, { encoding: 'utf8', flag: 'r' });
    resolve(data);
  } catch (err) {
    reject(err);
  }
});

methCall.then(
  data => console.log(data),
  err => console.log("Error reading file")
);
```

---

## 📡 `object.on()` — Listening for Events  
✅ Use `.on()` to define handlers for events like `data` or `end`.

```js
http.request(options, function(response) {
  let buffer = '';
  
  response.on('data', function(chunk) {
    buffer += chunk;
  });

  response.on('end', function() {
    console.log(buffer);
  });
}).end();
```

---

## 🧱 Callback Hell / Pyramid of Doom  
❌ Deeply nested callbacks reduce readability and maintainability.

```js
const makeCake = nextStep => {
  buyIngredients(function(shoppingList) {
    combineIngredients(bowl, mixer, function(ingredients) {
      bakeCake(oven, pan, function(batter) {
        decorate(icing, function(cake) {
          nextStep(cake);
        });
      });
    });
  });
};
```

---

## 🌐 Axios Request — Making HTTP Calls  
✅ Axios returns a promise and simplifies HTTP requests.

```js
const axios = require('axios').default;

function connectToURL(url) {
  axios.get(url)
    .then(resp => {
      console.log("Fulfilled");
      console.log(resp.data);
    })
    .catch(err => {
      console.log("Rejected");
    });
}

connectToURL('https://valid-url.com');
connectToURL('https://invalid-url.com');
```

---

# 📘 Glossary: Asynchronous I/O with Callback Programming  
Module 2 — Node.js & Express

| Term | Definition |
|--------------------|-----------------------------------------------------------------------------------------------------|
| Async | Short for "asynchronous" — tasks that run independently and don’t block other operations. |
| Axios Package | A library that wraps HTTP requests in promises, making async calls easier to manage. |
| Callback Hell | A situation where many nested callbacks make code hard to read and maintain. |
| Inversion of Control | When control of execution is handed off to another function or framework, often via callbacks. |
| Promise | A JavaScript object representing a future value. It can be pending, fulfilled, or rejected. |
| Pyramid of Doom | Another name for callback hell — visually shaped like a pyramid due to deep nesting. |
