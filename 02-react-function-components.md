## 🧠 Function Components with Array & DOM Manipulation

### 👉 Function Component (function keyword)
```jsx
import React from 'react'

function Extra() {
  return (
    <>
      <p>This is paragraph</p>
    </>
  )
}

export default Extra
```
Wraps JSX inside a named function and exports it by default.

---

### 👉 Function Component (arrow function)
```jsx
import React from 'react'

const Extra = () => {
  return (
    <div>Extra</div>
  )
}

export default Extra
```
Uses arrow syntax for cleaner, modern component declarations.

---

### 👉 Passing Props to Function Component
```jsx
import React from 'react'
import ChildComponent from './ChildComponent'

function ParentComponent () {
  let title = 'Project Manager'
  return (
    <>
      <ChildComponent title={title} />
    </>
  )
}

export default ParentComponent
```
Props are passed as attributes from parent to child.

---

### 👉 Accessing Props in Child Component
```jsx
import React from 'react'

const ChildComponent = (props) => {
  return (
    <>
      <p>The title is {props.title}</p>
    </>
  )
}

export default ChildComponent
```
Use `props.variableName` to access passed data.

---

### 👉 Event Handling in Function Component
```jsx
import React from 'react'

const Extra = (props) => {
  function show() {
    console.log('Show function')
  }

  return (
    <>
      <p>The title is {props.title}</p>
      <button onClick={() => show()}>Click Here</button>
    </>
  )
}

export default Extra
```
Define event handlers inside the component and bind them inline.

---

### 👉 State Management with useState
```jsx
import React, { useState } from 'react'

const StateManagement = () => {
  const [name, setName] = useState('John')

  return (
    <>
      <h1>State Management using useState</h1>
      <p>The name is {name}</p>
    </>
  )
}

export default StateManagement
```
useState hook enables dynamic state updates in function components.

---

### 👉 Array Declaration
```jsx
const names = ['Alice', 'Bob', 'Charlie']
```
Use square brackets to declare arrays.

---

### 👉 Stateful Array with useState
```jsx
const [todos, setTodos] = useState(['Learn React', 'Build Project'])
```
Manage array state with useState.

---

### 👉 Dynamically Constructed Arrays
```jsx
const numbers = []
for (let i = 0; i < 10; i++) {
  numbers.push(i)
}
```
Build arrays programmatically using loops.

---

### 👉 Array map() Method
```jsx
const items = ['Apple', 'Banana', 'Orange']
const itemList = items.map((item, index) => <li key={index}>{item}</li>)
return <ul>{itemList}</ul>
```
Use `.map()` to transform arrays into JSX elements.

---

### 👉 for...of Loop
```jsx
const items = ['Apple', 'Banana', 'Orange']
for (const item of items) {
  console.log(item)
}
```
Iterate over array elements with `for...of`.

---

### 👉 Rendering a List of Items
```jsx
import React from 'react'

function ArrayComponent() {
  const items = ['Autumn', 'Spring', 'Summer', 'Winter']
  return (
    <div>
      <h1>Seasons Names</h1>
      <ul>
        {items.map((item, index) => (
          <li key={index}>{item}</li>
        ))}
      </ul>
    </div>
  )
}

export default ArrayComponent
```
Use `.map()` to render lists dynamically.

---

### 👉 Add & Remove Items from Array
```jsx
import React, { useState } from 'react'

function MyComponent() {
  const [items, setItems] = useState(['Autumn', 'Spring', 'Winter', 'Summer'])
  const [inputValue, setInputValue] = useState('')

  const addItem = () => {
    setItems([...items, inputValue])
    setInputValue('')
  }

  const removeItem = (index) => {
    const newItems = [...items]
    newItems.splice(index, 1)
    setItems(newItems)
  }

  return (
    <div>
      <h1>Fruits</h1>
      <ul>
        {items.map((item, index) => (
          <li key={index}>
            {item}
            <button onClick={() => removeItem(index)}>Remove</button>
          </li>
        ))}
      </ul>
      <input
        type="text"
        value={inputValue}
        onChange={(e) => setInputValue(e.target.value)}
      />
      <button onClick={addItem}>Add</button>
    </div>
  )
}
```
Use spread syntax and `splice()` to manage array items.

---

### 👉 Conditional Rendering with Ternary
```jsx
import React, { useState } from 'react'

function ArrayComponent() {
  const [items, setItems] = useState(['React JS', 'Vue JS', 'Angular JS', 'Vanilla JS'])

  return (
    <div>
      <h1>Front End Languages</h1>
      {items.length > 0 ? (
        <ul>
          {items.map((item, index) => (
            <li key={index}>{item}</li>
          ))}
        </ul>
      ) : (
        <p>No Front End language is available</p>
      )}
    </div>
  )
}

export default ArrayComponent
```
Use ternary operator to conditionally render JSX.

---

### 👉 Inline Style in React
```jsx
import React from 'react'

function MyComponent() {
  return (
    <div style={{ backgroundColor: 'lightblue', padding: '20px', borderRadius: '5px' }}>
      <p style={{ color: 'white', fontSize: '18px' }}>
        This is a paragraph with inline styles.
      </p>
    </div>
  )
}

export default MyComponent
```
Apply styles directly using double curly braces.

---

### 👉 Style Using Object
```jsx
import React, { useState } from 'react'

function ToggleMessage() {
  const [isVisible, setIsVisible] = useState(true)

  const toggleVisibility = () => {
    setIsVisible(!isVisible)
  }

  const messageStyle = {
    display: isVisible ? 'block' : 'none',
    color: 'green',
    fontSize: '18px',
    marginTop: '10px'
  }

  return (
    <div>
      <h2>Toggle Message</h2>
      <button onClick={toggleVisibility}>
        {isVisible ? 'Hide Message' : 'Show Message'}
      </button>
      <p style={messageStyle}>This is a hidden message.</p>
    </div>
  )
}
```
Define style objects and apply them conditionally.

---

## 📘 Glossary of React Terms

## 📘 Glossary: Function Components with Array & DOM Manipulation

Welcome! This alphabetized glossary includes key terms used throughout the cheat sheet, plus additional industry-recognized concepts to support your React journey.

| Term                        | Definition                                                                                                                                       |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| Abstraction principle      | A principle that provides a way to make reusable components that encapsulate UI features.                                                       |
| Array                      | A data structure in JavaScript used to store multiple values in a single variable.                                                              |
| Array destructuring        | A feature that allows you to extract values from an array and assign them to individual variables.                                              |
| Array literal              | A syntax in JavaScript for creating arrays using square brackets and comma-separated values.                                                    |
| Attributes                 | Provide additional information about elements—such as properties, styles, or behavior.                                                          |
| Component composition      | Combining multiple smaller components to create complex functionality.                                                                          |
| Document object model (DOM)| An interface for web pages that represents HTML structure as a tree-like model.                                                                 |
| Elements                   | The building blocks of HTML documents.                                                                                                          |
| forEach()                  | A method that iterates over each element of an array and executes a callback function.                                                          |
| Hierarchy principle        | Organizes components in parent-child relationships for better structure and reuse.                                                              |
| Higher-order component     | A function that adds features like state or logic to components without modifying their implementation.                                         |
| Hook                       | A function that enables reuse of logic across components without changing hierarchy or nesting.                                                 |
| Initialization             | The phase where React runs the function body to set up the component’s initial structure and behavior.                                          |
| map()                      | A method used to iterate over an array and return a new array of React elements.                                                                |
| Mounting phase             | The lifecycle phase where React prepares and renders the component to the DOM.                                                                  |
| Props Default              | A fallback value for props using `defaultProps`, ensuring predictable rendering when props are missing.                                         |
| Properties (props)         | Data passed from parent to child components to enable customization and communication.                                                          |
| Rendering Array            | Dynamically generating elements based on array contents, often using `.map()` to return JSX.                                                    |
| Reuse principle            | Encourages reusing code chunks for better organization and maintainability.                                                                     |
| Side effects               | Operations like data fetching or DOM manipulation handled via `useEffect`, often with an empty dependency array.                                |
| State                      | The current condition or data of a component that influences its rendering and behavior.                                                        |
| State management           | Handling and updating component data over time in response to user actions or events.                                                           |
| State initialization       | Declaring and setting initial state variables using the `useState` hook.                                                                        |
| Updating phase             | React re-renders the component when state or props change, re-invoking the function body.                                                       |
| Unmounting phase           | Cleanup phase when React removes a component from the DOM.                                                                                      |
| useState hook              | A built-in React hook for managing state in function components. React re-renders the component when state updates.                             |
| Virtual DOM                | An in-memory representation of the real DOM, kept in sync by React’s reconciliation process.                                                    |

---
