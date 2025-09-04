```

🔁 useState() — Managing Component State The useState hook lets you declare and update local state inside function components. You can store strings, numbers, arrays, objects, or booleans.
jsx import React, { useState } from 'react';
function SideEffect() { const [empId, setEmpId] = useState(100); return <p>{empId}</p>; } `
✅ Use this to track dynamic values like form inputs, toggles, or counters.

⚡ useEffect() — Handling Side Effects useEffect runs code after the component renders. Perfect for fetching data, setting up subscriptions, or triggering animations.
jsx useEffect(() => { fetch('https://api.npoint.io/d542b9ad99f501ab3dbf') .then(res => res.json()) .then(data => setFoods(data)) .catch(err => console.error(err)); }, []); 
✅ The empty array [] ensures this runs only once when the component mounts.

🧩 Custom Hooks — Reusable Logic Custom hooks let you extract and reuse stateful logic across components.
UseToggle.jsx `jsx import { useState } from "react";
function UseToggle(initialValue = false) { const [value, setValue] = useState(initialValue); const toggle = () => setValue(!value); return [value, toggle]; } export default UseToggle; `
ToggleButton.jsx `jsx import UseToggle from './UseToggle';
function ToggleButton() { const [isToggled, toggle] = UseToggle(false); return <button onClick={toggle}>{isToggled ? 'ON' : 'OFF'}</button>; } `
✅ Great for toggles, modals, or any binary state.

🌐 Fetch API — Basic Data Retrieval Use the browser-native fetch() to get data from an API.
js fetch('https://jsonplaceholder.typicode.com/posts') .then(res => res.json()) .then(data => console.log(data)) .catch(err => console.error(err)); 
✅ Simple and built-in, but lacks advanced features like interceptors.

🚀 Axios — Enhanced API Requests Axios is a promise-based HTTP client with cleaner syntax and better error handling.
js import axios from 'axios';
axios.get('https://jsonplaceholder.typicode.com/posts') .then(res => console.log(res.data)) .catch(err => console.error(err)); `
✅ Supports request cancellation, interceptors, and automatic JSON parsing.

✍️ onChange — Tracking Input Changes Use onChange to update state as the user types.
jsx function FormData() { const [empName, setEmpName] = useState('');
const handleChange = (e) => setEmpName(e.target.value); const handleSubmit = (e) => { e.preventDefault(); console.log('Form submitted:', empName); };
return ( <form onSubmit={handleSubmit}> <input type="text" value={empName} onChange={handleChange} /> <button type="submit">Submit</button> </form> ); } `
✅ Essential for controlled components and form validation.

🧰 Redux Toolkit — Simplified State Management Install Redux Toolkit to streamline Redux setup:
bash npm install @reduxjs/toolkit 
✅ Includes built-in reducers, dev tools integration, and async logic via createAsyncThunk.

