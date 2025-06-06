<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>To-Do List App</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f4f4f4;
      display: flex;
      flex-direction: column;
      align-items: center;
      padding: 40px;
    }

    h1 {
      color: #333;
    }

    #todo-container {
      background: #fff;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 2px 8px rgba(0, 0, 0, 0.2);
      width: 300px;
    }

    input[type="text"] {
      width: 70%;
      padding: 8px;
      margin-right: 5px;
    }

    button {
      padding: 8px 10px;
      cursor: pointer;
      background-color: #28a745;
      color: white;
      border: none;
      border-radius: 5px;
    }

    ul {
      list-style: none;
      padding: 0;
      margin-top: 20px;
    }

    li {
      padding: 8px;
      background: #eee;
      margin-bottom: 8px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      border-radius: 4px;
    }

    .completed {
      text-decoration: line-through;
      color: gray;
    }

    .remove-btn {
      background-color: #dc3545;
      padding: 4px 8px;
      border: none;
      border-radius: 4px;
      color: white;
      cursor: pointer;
    }
  </style>
</head>
<body>

  <h1>To-Do List</h1>
  <div id="todo-container">
    <input type="text" id="taskInput" placeholder="Enter a task" />
    <button id="addTaskBtn">Add</button>
    <ul id="taskList"></ul>
  </div>

  <script>
    const addTaskBtn = document.getElementById("addTaskBtn");
    const taskInput = document.getElementById("taskInput");
    const taskList = document.getElementById("taskList");

    addTaskBtn.addEventListener("click", () => {
      const taskText = taskInput.value.trim();
      if (taskText !== "") {
        const li = document.createElement("li");

        const taskSpan = document.createElement("span");
        taskSpan.textContent = taskText;
        taskSpan.addEventListener("click", () => {
          taskSpan.classList.toggle("completed");
        });

        const removeBtn = document.createElement("button");
        removeBtn.textContent = "X";
        removeBtn.classList.add("remove-btn");
        removeBtn.addEventListener("click", () => {
          taskList.removeChild(li);
        });

        li.appendChild(taskSpan);
        li.appendChild(removeBtn);
        taskList.appendChild(li);

        taskInput.value = "";
        taskInput.focus();
      }
    });
  </script>

</body>
</html>
