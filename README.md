# Ex03 To-Do List using JavaScript
## Date:16.03.2025
NAME : JESLIN GNANASHEELA M

REG NO : 212222040062

## AIM
To create a To-do Application with all features using JavaScript.

## ALGORITHM
### STEP 1
Build the HTML structure (index.html).

### STEP 2
Style the App (style.css).

### STEP 3
Plan the features the To-Do App should have.

### STEP 4
Create a To-do application using Javascript.

### STEP 5
Add functionalities.

### STEP 6
Test the App.

### STEP 7
Open the HTML file in a browser to check layout and functionality.

### STEP 8
Fix styling issues and refine content placement.

### STEP 9
Deploy the website.

### STEP 10
Upload to GitHub Pages for free hosting.

## PROGRAM
# App.js
```
import React, { useState } from "react";
import "./App.css";

function App() {
  const [tasks, setTasks] = useState([]);
  const [input, setInput] = useState("");

  const addTask = () => {
    if (input.trim() === "") return;
    setTasks([...tasks, input]);
    setInput("");
  };

  const deleteTask = (index) => {
    const newTasks = tasks.filter((_, i) => i !== index);
    setTasks(newTasks);
  };

  const toggleComplete = (index) => {
    const updated = [...tasks];
    updated[index] = {
      text: updated[index].text || updated[index],
      completed: !updated[index].completed,
    };
    setTasks(updated);
  };

  return (
    <>
      <div className="container">
        <h1>To-Do List</h1>
        <div className="input-section">
          <input
            type="text"
            value={input}
            onChange={(e) => setInput(e.target.value)}
            placeholder="Add a new task..."
          />
          <button onClick={addTask}>Add</button>
        </div>
        <ul>
          {tasks.map((task, index) => {
            const isCompleted = task.completed;
            const taskText = task.text || task;
            return (
              <li
                key={index}
                className={isCompleted ? "completed" : ""}
                onClick={() => toggleComplete(index)}
              >
                {taskText}
                <button
                  onClick={(e) => {
                    e.stopPropagation();
                    deleteTask(index);
                  }}
                >
                  X
                </button>
              </li>
            );
          })}
        </ul>
      </div>

      {/* Footer Section */}
      <footer className="footer">
        <p>&copy;Jeslin Gnanasheela M(212222040062)</p>
      </footer>
    </>
  );
}

export default App;

```
# App.css
```
body {
  font-family: Arial, sans-serif;
  background-color: #f4f6f8;
  margin: 0;
  padding: 50px 0 70px 0; /* top, right/left, bottom */
}


.container {
  background: white;
  padding: 30px;
  border-radius: 15px;
  box-shadow: 0 5px 15px rgba(0,0,0,0.1);
  width: 350px;
  margin: auto;
}

h1 {
  text-align: center;
  margin-bottom: 20px;
  color: #333;
}

.input-section {
  display: flex;
  gap: 10px;
  margin-bottom: 20px;
}

input[type="text"] {
  flex: 1;
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 8px;
}

button {
  padding: 10px 15px;
  background-color: #007bff;
  color: white;
  border: none;
  border-radius: 8px;
  cursor: pointer;
}

button:hover {
  background-color: #0056b3;
}

ul {
  list-style: none;
  padding: 0;
}

li {
  background: #f0f0f0;
  margin-bottom: 10px;
  padding: 12px;
  border-radius: 8px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

li.completed {
  text-decoration: line-through;
  color: #888;
  background-color: #dcdcdc;
}

li button {
  background: red;
  border: none;
  color: white;
  padding: 5px 8px;
  border-radius: 6px;
  cursor: pointer;
}

/* ✅ Footer Styles */
/* Fixed Footer at Bottom */
.footer {
  position: fixed;
  bottom: 0;
  left: 0;
  width: 100%;
  background-color: #ffffff;
  text-align: center;
  padding: 10px 0;
  font-size: 14px;
  color: #666;
  border-top: 1px solid #ddd;
  box-shadow: 0 -1px 5px rgba(0, 0, 0, 0.1);
}


```


## OUTPUT
![ex3 web](https://github.com/user-attachments/assets/fd6d6133-6f7f-4d03-8dde-9450d77eb936)


## RESULT
The program for creating To-do list using JavaScript is executed successfully.
