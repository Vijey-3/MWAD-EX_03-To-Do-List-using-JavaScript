# MWAD-EX_03-To-Do-List-using-JavaScript
## Date:

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
### index.html
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>To-Do List</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="container">
    <h1>To-Do List</h1>
    <div class="input-section">
      <input type="text" id="task-input" placeholder="Enter a new task">
      <button id="add-task">Add</button>
    </div>
    <ul id="task-list"></ul>
  </div>
  <script src="script.js"></script>
</body>
</html>
```
### style.css
```
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Arial, sans-serif;
  background: #f4f4f9;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

.container {
  background: #fff;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0,0,0,0.2);
  width: 350px;
  text-align: center;
}

h1 {
  margin-bottom: 20px;
  color: #333;
}

.input-section {
  display: flex;
  gap: 10px;
}

#task-input {
  flex: 1;
  padding: 10px;
  border: 1px solid #ddd;
  border-radius: 5px;
}

#add-task {
  padding: 10px 15px;
  background: #4caf50;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

#add-task:hover {
  background: #45a049;
}

#task-list {
  margin-top: 20px;
  list-style: none;
  padding: 0;
}

#task-list li {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background: #fafafa;
  padding: 10px;
  margin-bottom: 8px;
  border-radius: 5px;
  border: 1px solid #ddd;
}

#task-list li.completed {
  text-decoration: line-through;
  color: gray;
}

button.delete {
  background: #e53935;
  border: none;
  color: white;
  padding: 5px 10px;
  border-radius: 5px;
  cursor: pointer;
}
```
### script.js
```
const addTaskBtn = document.getElementById("add-task");
const taskInput = document.getElementById("task-input");
const taskList = document.getElementById("task-list");

addTaskBtn.addEventListener("click", addTask);

function addTask() {
  const taskText = taskInput.value.trim();

  if (taskText === "") {
    alert("Please enter a task!");
    return;
  }

  const li = document.createElement("li");

  const span = document.createElement("span");
  span.textContent = taskText;
  span.addEventListener("click", () => {
    li.classList.toggle("completed");
  });

  const deleteBtn = document.createElement("button");
  deleteBtn.textContent = "Delete";
  deleteBtn.classList.add("delete");
  deleteBtn.addEventListener("click", () => {
    li.remove();
  });

  li.appendChild(span);
  li.appendChild(deleteBtn);
  taskList.appendChild(li);

  taskInput.value = "";
}
```

## OUTPUT
<img width="1908" height="916" alt="Screenshot 2025-09-17 084328" src="https://github.com/user-attachments/assets/1ab0d6fe-0cb2-430f-bb43-65f336d56539" />
<img width="1909" height="900" alt="Screenshot 2025-09-17 084545" src="https://github.com/user-attachments/assets/3d4a0f78-0f82-466d-b056-0b5a73a08c35" />


## RESULT
The program for creating To-do list using JavaScript is executed successfully.
