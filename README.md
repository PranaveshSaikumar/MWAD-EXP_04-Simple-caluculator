# MWAD-EXP_04-Simple-caluculator
## Date: 17-11-25

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
```
Calc.jsx
import { useState } from "react";
import "../EXPS/Calc.css";

export default function Calculator() {
  const [value, setValue] = useState("");

  const handleClick = (val) => {
    setValue(value + val);
  };

  const calculate = () => {
    try {
      setValue(eval(value).toString());
    } catch {
      setValue("Error");
    }
  };

  const clearDisplay = () => {
    setValue("");
  };

  return (
    <div className="calc-container">
      <input className="display" type="text" value={value} readOnly />

      <div className="buttons">
        <button onClick={() => handleClick("7")}>7</button>
        <button onClick={() => handleClick("8")}>8</button>
        <button onClick={() => handleClick("9")}>9</button>
        <button onClick={() => handleClick("/")}>/</button>

        <button onClick={() => handleClick("4")}>4</button>
        <button onClick={() => handleClick("5")}>5</button>
        <button onClick={() => handleClick("6")}>6</button>
        <button onClick={() => handleClick("*")}>*</button>

        <button onClick={() => handleClick("1")}>1</button>
        <button onClick={() => handleClick("2")}>2</button>
        <button onClick={() => handleClick("3")}>3</button>
        <button onClick={() => handleClick("-")}>-</button>

        <button onClick={clearDisplay}>C</button>
        <button onClick={() => handleClick("0")}>0</button>
        <button onClick={calculate}>=</button>
        <button onClick={() => handleClick("+")}>+</button>
      </div>
    </div>
  );
}
```
```
Calc.css
.calc-container {
  width: 260px;
  margin: 40px auto;
  padding: 20px;
  border-radius: 12px;
  background: #f3f3f3;
  box-shadow: 0px 0px 10px gray;
}

.display {
  width: 100%;
  height: 50px;
  font-size: 22px;
  margin-bottom: 15px;
  padding: 10px;
  text-align: right;
  border-radius: 8px;
  border: 1px solid #ccc;
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 10px;
}

button {
  height: 45px;
  font-size: 18px;
  border: none;
  border-radius: 8px;
  background: #ddd;
  cursor: pointer;
}

button:hover {
  background: #ccc;
}
```
```
App.jsx
import Calculator from "./EXPS/Calc.jsx";

export default function App() {
  return (
    <div>
      <Calculator />
    </div>
  );
}
```


## OUTPUT

<img width="696" height="641" alt="image" src="https://github.com/user-attachments/assets/85671a6b-9639-49eb-aab9-d47577675bd8" />


## RESULT
The program for developing a simple calculator in React.js is executed successfully.
