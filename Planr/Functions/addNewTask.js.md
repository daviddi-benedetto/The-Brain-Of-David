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
//  ______   ______     ______     __  __     ______
// /\__  _\ /\  __ \   /\  ___\   /\ \/ /    /\  ___\
// \/_/\ \/ \ \  __ \  \ \___  \  \ \  _"-.  \ \___  \
//    \ \_\  \ \_\ \_\  \/\_____\  \ \_\ \_\  \/\_____\
//     \/_/   \/_/\/_/   \/_____/   \/_/\/_/   \/_____/
//

// Get the plus button and assign it to a variable
const addNewTaskButton = document.querySelector(".plus-header");
// ADD NEW TASK FUNCTION
function addNewTask() {
    // Make a new div for the task and give it a class
    const taskDiv = document.createElement("div");
    taskDiv.className = "task";

    // Set the HTML content for the new task
    taskDiv.innerHTML = `
        <i class="fa-regular fa-circle task-icon-incomplete"></i>
        <div class="task-text" contenteditable="true"></div>
        <i class="fa-solid fa-xmark"></i>
    `;

    // Append the new task to the task list
    document.getElementById("task-list").appendChild(taskDiv);

    // Add event listener to the delete button of the new task and make it remove its own div when clicked
    taskDiv.querySelector(".fa-xmark").addEventListener("click", function() {
        this.parentElement.remove();
    });


    // Add event listener to stop enter key making text box larger
    taskDiv.querySelector(".task-text").addEventListener("keypress", e => {
        if (e.key === "Enter") {
            e.preventDefault(); // This prevents the enter key from making a new line
        }
    });
} 

// Event listener for adding a new task on click

addNewTaskButton.addEventListener("click", addNewTask);
```

To remove a task, see [[deleteTask.js]]