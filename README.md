# Ex04 Simple Calculator - React Project


## AIM
To  develop a Simple Calculator using React.js with clean and responsive design, ensuring a smooth user experience across different screen sizes.

## ALGORITHM
### STEP 1
Create a React App.

### STEP 2
Open a terminal and run:
  <ul><li>npx create-react-app simple-calculator</li>
  <li>cd simple-calculator</li>
  <li>npm start</li></ul>

### STEP 3
Inside the src/ folder, create a new file Calculator.js and define the basic structure.

### STEP 4
Plan the UI: Display screen, number buttons (0-9), operators (+, -, *, /), clear (C), and equal (=).

### STEP 5
Create a new file Calculator.css in src/ and add the styling.

### STEP 6
Open src/App.js and modify it.

### STEP 7
Start the development server.
  npm start

### STEP 8
Open http://localhost:3000/ in the browser.

### STEP 9
Test the calculator by entering numbers and operations.

### STEP 10
Fix styling issues and refine content placement.

### STEP 11
Deploy the website.

### STEP 12
Upload to GitHub Pages for free hosting.

## PROGRAM

App.jsx

```jsx

import React, { useState } from "react";
import './App.css';

function App() {

  const [input,setInput] = useState("");

  const HandleInput = (value) => {
      setInput((prev) => prev+value); 
  }

  const HandleClear = () => {
    setInput("");
  }

  const HandleCalculate = () =>
  {
    const result = eval(input);
    setInput(result.toString());
  }
  
  return(
    <div>
      <input type="text" value={input}/><br></br>
      <button onClick={() => HandleInput("7")}>7</button>
      <button onClick={() => HandleInput("8")}>8</button>
      <button onClick={() => HandleInput("9")}>9</button>
      <button onClick={() => HandleInput("+")}>+</button><br></br>
      <button onClick={() => HandleInput("4")}>4</button>
      <button onClick={() => HandleInput("5")}>5</button>
      <button onClick={() => HandleInput("6")}>6</button>
      <button onClick={() => HandleInput("-")}>-</button><br></br>
      <button onClick={() => HandleInput("1")}>1</button>
      <button onClick={() => HandleInput("2")}>2</button>
      <button onClick={() => HandleInput("3")}>3</button>
      <button onClick={() => HandleInput("*")}>*</button><br></br>
      <button onClick={HandleClear}>C</button>
      <button onClick={() => HandleInput("0")}>0</button>
      <button onClick={HandleCalculate}>=</button>
      <button onClick={() => HandleInput("/")}>/</button>
    </div>
  );
}


  
export default App;


```


Main.jsx
```jsx

import { useState } from 'react'
import { StrictMode } from 'react'
import { createRoot } from 'react-dom/client'
import './index.css'
import App from './App.jsx'

createRoot(document.getElementById('root')).render(
  <StrictMode>
    <App />
  </StrictMode>
)

```
## OUTPUT

<img width="1919" height="1141" alt="image" src="https://github.com/user-attachments/assets/d3c40a1b-3ba1-4f52-9982-7539135646a0" />

<img width="1919" height="1136" alt="image" src="https://github.com/user-attachments/assets/31fb26fc-7fb3-4366-aa6e-60250f2e1aaa" />

<img width="1919" height="1137" alt="image" src="https://github.com/user-attachments/assets/273da2b3-e158-43da-97b3-767d5f1a7699" />

## RESULT
The program for developing a simple calculator in React.js is executed successfully.
