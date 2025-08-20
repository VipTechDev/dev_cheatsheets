// 👉 Vite Setup
npm create vite@latest // Create a new React project using Vite

// 👉 JSX Syntax
<>...</> // Fragment syntax: wrap multiple elements without adding extra nodes
<div>...</div> // Parent tag syntax: wrap multiple elements inside a single tag

// 👉 Class Component Basics
import React, { Component } from 'react' // Import React and Component
export default class Extra extends Component {
  render() {
    return (
      <>
        <p>This is class component</p>
      </>
    )
  }
}

// 👉 State Management in Class Component
constructor() {
  super()
  this.state = {
    count: 0 // Initial state value
  }
}

// 👉 Accessing State in Render
<p>The count is {this.state.count}</p> // Use curly braces to access state

// 👉 Props in Class Component
// Parent Component
<Extra title={this.state.title} /> // Pass props as attributes

// Child Component
constructor(props) {
  super()
}
<p>The count value is {this.props.title}</p> // Access props via this.props

// 👉 Event Handling in Class Component
handleClick() {
  alert('Button clicked!') // Define event handler
}
<button onClick={this.handleClick}>Click Me</button> // Bind event to handler
