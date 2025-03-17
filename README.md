# Ex03 To-Do List using JavaScript
## Date:16.03.20205
NAME : DHAREENE R K
REG NO : 212222040035
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
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>To-Do List</title>
    <style>
        /* General Styling */
        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(to right, #ff9a9e, #fad0c4);
            text-align: center;
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            min-height: 100vh;
        }

        /* Container */
        .container {
            background: white;
            max-width: 400px;
            margin: auto;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
        }

        h1 {
            color: #333;
            font-size: 24px;
        }

        /* Input Section */
        .todo-input {
            display: flex;
            gap: 10px;
            justify-content: center;
            margin-bottom: 15px;
        }

        input {
            width: 70%;
            padding: 10px;
            border: 2px solid #ff758c;
            border-radius: 5px;
            font-size: 16px;
        }

        /* Add Button */
        button {
            padding: 10px;
            border: none;
            background: #ff758c;
            color: white;
            cursor: pointer;
            border-radius: 5px;
            font-size: 16px;
            transition: 0.3s;
        }

        button:hover {
            background: #ff416c;
        }

        /* Task List */
        ul {
            list-style: none;
            padding: 0;
        }

        li {
            background: #fff;
            padding: 10px;
            margin: 10px 0;
            border-radius: 5px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
            transition: 0.3s ease-in-out;
        }

        li:hover {
            transform: scale(1.02);
        }

        /* Delete Button */
        .delete-btn {
            background: #ff4d4d;
            color: white;
            border: none;
            padding: 5px 10px;
            border-radius: 5px;
            cursor: pointer;
            font-size: 14px;
            transition: 0.3s;
        }

        .delete-btn:hover {
            background: #d63333;
        }

        /* Sticky Footer */
        footer {
            margin-top: auto;
            padding: 15px;
            background: #333;
            color: white;
            font-size: 14px;
            text-align: center;
            position: relative;
            width: 100%;
        }
    </style>
</head>
<body>

    <div class="container">
        <h1>📝 To-Do List</h1>
        <div class="todo-input">
            <input type="text" id="taskInput" placeholder="Enter a task...">
            <button onclick="addTask()">Add</button>
        </div>
        <ul id="taskList"></ul>
    </div>

    <footer>
        © 2025 Dhareene R K 212222040035  | All rights reserved. 
    </footer>

    <script>
        function addTask() {
            let taskInput = document.getElementById("taskInput");
            let taskList = document.getElementById("taskList");

            if (taskInput.value.trim() === "") {
                alert("Please enter a task!");
                return;
            }

            let li = document.createElement("li");
            li.innerHTML = `
                ${taskInput.value} 
                <button class="delete-btn" onclick="deleteTask(this)">Delete</button>
            `;

            taskList.appendChild(li);
            taskInput.value = "";
        }

        function deleteTask(button) {
            let taskList = document.getElementById("taskList");
            taskList.removeChild(button.parentElement);
        }
    </script>

</body>
</html>

```

## OUTPUT:
![dhareeneweb3 sc1](https://github.com/user-attachments/assets/04241e00-75d7-4cf4-bb0a-40200e120053)




## RESULT
The program for creating To-do list using JavaScript is executed successfully.
++
