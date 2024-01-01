# addNewTask.js
The addNewTask function is dependent on the task-container.html it is inside of. Goal and pseudocode below. 

### Goal
I have the html of an individual task that I want to be duplicated into the task-container whenever the function is called (in theory with the + sign in the task container). This task container needs to become its own div element that can save its inside text value independent of the other tasks.

### Prerequisites
Inside the task-container.html there is a div element with a class of "task-list". This is where the each task.html div will be summoned. One task div is already there so when a new container is made, it isn't empty.

```js
<!-- Tasks -->
<div id="task-list" class="task-list">
    <div class="task">
        <i class="fa-regular fa-circle task-icon-incomplete"></i>
        <div class="task-text" contenteditable="true"></div>
        <i id="task-delete" class="fa-solid fa-xmark" onclick="deleteTask()"></i>
    </div>
</div>
```

### Pseudocode
1. Create a new div element and assign it to a variable.
2. Assign the div element with the class "task".
3. Create a variable with HTML inside of it.
4. Append the task variable with the HTML variable such to fill the task div with the HTML.
5. Import the "task-list" div into the JS and assign the element to a variable.
6. Append the "task" variable to the end of the "task-list" variable.
7. Save the "task-list" div to the browser memory.

### Code

```js
function addNewTask() {
    // Create taskDiv, then give it class of "task"
    const taskDiv = document.createElement("div");
    taskDiv.setAttribute("class", "task");
    

    // Put html into a variable called taskHTML
    // Then says the inside HTML content of the taskDiv is whats inside the taskHTML variable
    const taskHTML = `
    <i class="fa-regular fa-circle task-icon-incomplete"></i>
    <div class="task-text" contenteditable="true"></div>
    <i id="task-delete" class="fa-solid fa-xmark" onclick="deleteTask()"></i>
    `;
    taskDiv.innerHTML=taskHTML;

    // Finds the div with the id "task-list" and creates a variable for it
    const taskListDiv = document.getElementById("task-list");
    taskListDiv.append(taskDiv);
}
```

To remove a task, see [[deleteTask.js]]