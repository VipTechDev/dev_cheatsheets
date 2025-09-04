## ⚙️ JavaScript Cheat Sheet  
DOM Manipulation, Traversal, Events, Arrays, Dates, Browser Info, and More

---

### 🧱 DOM Manipulation  
```js
document.createElement("p"); // Creates a <p> element
document.createTextNode("Hello World"); // Creates a text node
document.body.appendChild(newPara); // Appends element to body
document.getElementById("div1").innerHTML = "<p>Hello World!</p>"; // Sets HTML
document.getElementById("div1").getAttribute("style"); // Gets attribute value
document.getElementById("div1").removeAttribute("style"); // Removes attribute
document.getElementById("theImage").setAttribute("src", "another.gif"); // Sets attribute
document.getElementById("div1").style.color = "red"; // Changes style
```  
✅ Create, modify, and style elements dynamically.

---

### 🔍 DOM Traversal  
```js
document.getElementsByTagName("p"); // Gets all <p> elements
document.forms["form1"].elements["field1"]; // Access form field
```  
✅ Navigate and access elements with precision.

---

### 🎯 DOM Events  
```js
document.getElementById("MyHTMLPage").onload = function () { myFunction }; // onload event
```  
✅ Trigger actions when the page or elements load.

---

### 🧬 DOM Node Operations  
```js
let newLI = document.createElement("li");
newLI.innerText = "new Element";
let elementList = document.getElementById("thisList");
elementList.insertBefore(newLI, elementList.childNodes[0]); // insertBefore

let secondBullet = document.createTextNode("blue");
let myList = document.getElementById("thisList").childNodes[1];
myList.replaceChild(secondBullet, myList.childNodes[1]); // replaceChild
```  
✅ Insert and replace nodes to reshape the DOM.

---

### 🎵 Array Example  
```js
const Beatles = ["Ringo", "Paul", "George", "John"];
console.log(Beatles[0]); // "Ringo"
```  
✅ Store and access data in indexed collections.

---

### 📅 Date Object  
```js
let date1 = new Date("2021-1-17 13:15:30");
let date2 = new Date(2021, 0, 17); // Month is zero-based
```  
✅ Work with time, dates, and scheduling logic.

---

### 🌍 Window & Browser Info  
```js
window.open("http://www.w3schools.com"); // Opens new window
window.scrollTo(20, 200); // Scrolls window
let screenWidth = screen.width;
let screenHeight = screen.height;
let hostname = location.hostname;
let browser = navigator.appName;
```  
✅ Interact with browser and screen properties.

---

### ⏪ History Navigation  
```js
history.go(-2); // Go back 2 pages
```  
✅ Navigate browser history programmatically.

---

### 🛡️ Error Handling  
```js
try {
  // code that might throw
} catch (err) {
  document.getElementById("myfile").innerHTML = err.name;
  throw new Error("Only values 1-10 are permitted");
}
```  
✅ Catch and handle errors gracefully.

---

### 🔍 Primitive Wrapping & typeof  
```js
let n = new String("abc");
console.log(typeof "abc"); // "string"
console.log(typeof n); // "object"
```  
✅ Understand type coercion and object wrapping.

---

### ⚠️ Testing Output (use sparingly!)  
```js
document.write("Hello World"); // Overwrites document
```  
✅ Use with caution—can overwrite your entire page.
