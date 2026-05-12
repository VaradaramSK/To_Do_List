# Ex03 To-Do List using JavaScript
## Date:10-03-2026

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

### HTML:
```html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>To Do List</title>

    <link rel="stylesheet" href="style.css">
</head>
<body>

    <div class="container">
        <h1>To Do List</h1>

        <div class="input-section">
            <input type="text" id="taskInput" placeholder="Enter a task">
            <button onclick="addTask()">Add</button>
        </div>

        <ul id="taskList"></ul>
    </div>

    <script src="script.js"></script>
</body>
</html>
```

### CSS:
```css
body {
    font-family: Arial, sans-serif;
    background-color: #f0f0f0;

    display: flex;
    justify-content: center;
    align-items: center;

    height: 100vh;
}

.container {
    background-color: white;
    padding: 20px;
    width: 350px;

    border-radius: 10px;
    box-shadow: 0px 0px 10px gray;
}

h1 {
    text-align: center;
}

.input-section {
    display: flex;
    gap: 10px;
}

input {
    flex: 1;
    padding: 10px;
}

button {
    padding: 10px 15px;
    background-color: green;
    color: white;

    border: none;
    border-radius: 5px;

    cursor: pointer;
}

button:hover {
    background-color: darkgreen;
}

ul {
    list-style: none;
    padding: 0;

    margin-top: 20px;
}

li {
    background-color: #eeeeee;
    padding: 10px;
    margin-top: 10px;

    display: flex;
    justify-content: space-between;
    align-items: center;

    border-radius: 5px;
}

.delete-btn {
    background-color: red;
}

.delete-btn:hover {
    background-color: darkred;
}
```

### JavaScript:
```js
function addTask() {

    let input = document.getElementById("taskInput");
    let task = input.value;

    if (task === "") {
        alert("Please enter a task");
        return;
    }

    let li = document.createElement("li");

    li.innerHTML = `
        ${task}
        <button class="delete-btn" onclick="removeTask(this)">
            Delete
        </button>
    `;

    document.getElementById("taskList").appendChild(li);

    input.value = "";
}

function removeTask(button) {
    button.parentElement.remove();
}
```

## OUTPUT

<img width="1920" height="1080" alt="Screenshot (279)" src="https://github.com/user-attachments/assets/acb74b33-fe9c-4439-95a8-50b97fd9426e" />


<img width="1920" height="1080" alt="Screenshot (280)" src="https://github.com/user-attachments/assets/feddcc9c-271a-4222-9b7a-882c1042c48b" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/16762a1d-0456-443a-acbc-35dc89d06382" />

## RESULT
The program for creating To-do list using JavaScript is executed successfully.
