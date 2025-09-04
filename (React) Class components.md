## 🧠 React Class Component Cheat Sheet  
Vite Setup, JSX Syntax, State, Props, Events, and Glossary

---

### ⚡ Vite Setup  
```bash
npm create vite@latest
```  
✅ Create a new React project using Vite.

---

### 🔧 JSX Syntax  
```jsx
<>...</> // Fragment syntax: wrap multiple elements without adding extra nodes
<div>...</div> // Parent tag syntax: wrap multiple elements inside a single tag
```  
✅ Use fragments or divs to group JSX elements.

---

### 🧱 Class Component Basics  
```jsx
import React, { Component } from 'react';

export default class Extra extends Component {
  render() {
    return (
      <>
        <p>This is class component</p>
      </>
    );
  }
}
```  
✅ Use `Component` from React to define class-based components.

---

### 🧮 State Management in Class Component  
```jsx
constructor() {
  super();
  this.state = {
    count: 0 // Initial state value
  };
}
```  
✅ Initialize state inside the constructor using `this.state`.

---

### 📊 Accessing State in Render  
```jsx
<p>The count is {this.state.count}</p>
```  
✅ Use curly braces to access state values in JSX.

---

### 📦 Props in Class Component  

**Parent Component**  
```jsx
<Extra title={this.state.title} />
```  
✅ Pass props as attributes.

**Child Component**  
```jsx
constructor(props) {
  super();
}
<p>The count value is {this.props.title}</p>
```  
✅ Access props via `this.props`.

---

### 🖱️ Event Handling in Class Component  
```jsx
handleClick() {
  alert('Button clicked!');
}

<button onClick={this.handleClick}>Click Me</button>
```  
✅ Define event handlers and bind them to JSX elements.

---

## 📘 Glossary of React Terms  

| Term                 | Definition                                                                 |
|----------------------|----------------------------------------------------------------------------|
| App.jsx              | Root component of the React application                                   |
| Babel                | Compiles JSX code into browser-compatible JavaScript                      |
| Class                | Blueprint for creating objects in JavaScript                              |
| const                | Declares constants that cannot be reassigned                              |
| eslintrc.cjs         | ESLint config file using CommonJS module format                           |
| ECMAScript 6 (ES6)   | JavaScript standard released in 2015 by Ecma International                |
| Framework            | Foundation for building complete software applications                    |
| Front-end framework  | Focuses on building the user-facing side of web apps                      |
| .gitignore           | Specifies files/folders Git should ignore                                 |
| Hook                 | React feature for managing state and side effects in functional components|
| Index.html           | Entry point HTML file for web applications                                |
| JavaScript XML (JSX) | Syntax extension allowing HTML-like code in JavaScript                    |
| let                  | Declares block-scoped variables                                           |
| main.jsx             | Entry point for React rendering logic                                     |
| Node modules         | Directory containing installed npm/yarn dependencies                      |
| package.json         | Metadata and dependency list for the project                              |
| Public directory     | Stores static assets like HTML, images, and fonts                         |
| React                | JavaScript library for building dynamic user interfaces                   |
| README.md            | Project documentation file with setup and usage info                      |
| src directory        | Contains the source code of the React app                                 |
| Subclass             | Class that inherits from another class                                    |
| Superclass           | Class being inherited by a subclass                                       |
| this                 | Refers to the current object context                                      |
| var                  | Declares variables with function or global scope                          |
| Vite                 | Fast build tool leveraging native ES modules                              |
| vite.config.js       | Configuration file for Vite build settings                                |
