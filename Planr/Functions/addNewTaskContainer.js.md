# addNewTaskContainer.js
### Goal
The task container works similarly to that of the tasks themselves from the [[addNewTask.js]] function, but is just a lower level of organization. When this function is called, a new div needs to be created for the tasks to be stored in.
### Prerequisites
This is the task-container html that will be reused.

```js
<!--- Task-Container Below --->
<div class="task-list-container">
	<!-- Task List Header -->
	<div class="task-list-header">
		<div class="task-list-header-left-side">
			<i class="fa-solid fa-caret-up"></i>
			<h2 id="task-list-header-text">New Project</h2>
		</div>
		<div class="task-list-header-right-side">
			<i id="task-list-header-plus" class="fa-solid fa-plus plus-header"></i>
			<p id="task-list-header-counter">0/0</p>
			<i id="task-list-header-delete" class="fa-solid fa-xmark x-header"></i>
		</div>
	</div>

	<!-- Tasks -->
	<div id="task-list" class="task-list"></div>
</div>
```

### Back End Pseudocode
1. Create a new csv file with the project name as the file name.
### Front End Pseudocode
1. Create a new div element and assign it to a variable.
2. Assign the div element with the class "task-list-container".
3. Create a variable with HTML inside of it.
4. Append the task variable with the HTML variable such to fill the task div with the HTML.
5. Import the "task-list" div into the JS and assign the element to a variable.
6. Append the "task" variable to the end of the "task-list" variable.
7. Save the "task-list" div to the browser memory.

### Code

```js
//      _       _     _    ______       _      _         _____         _           ____            _        _
//     / \   __| | __| |  / /  _ \  ___| | ___| |_ ___  |_   _|_ _ ___| | _____   / ___|___  _ __ | |_ __ _(_)_ __   ___ _ __
//    / _ \ / _` |/ _` | / /| | | |/ _ \ |/ _ \ __/ _ \   | |/ _` / __| |/ / __| | |   / _ \| '_ \| __/ _` | | '_ \ / _ \ '__|
//   / ___ \ (_| | (_| |/ / | |_| |  __/ |  __/ ||  __/   | | (_| \__ \   <\__ \ | |__| (_) | | | | || (_| | | | | |  __/ |
//  /_/   \_\__,_|\__,_/_/  |____/ \___|_|\___|\__\___|   |_|\__,_|___/_|\_\___/  \____\___/|_| |_|\__\__,_|_|_| |_|\___|_|
//

const addNewTaskContainerButton = document.querySelector(".fa-circle-plus");

// ADD NEW TASK CONTAINER FUNCTION
function addNewTaskContainer() {
    /// BACK END ///

    /// FRONT END ///
    // Make a new div for the task and give it a class
    const taskContainerDiv = document.createElement("div");
    taskContainerDiv.className = "task-list-container";

    // Set the HTML content for the new task CONTAINER
    taskContainerDiv.innerHTML = `
    <!--- Task-Container Below --->
    <div class="tasks-container">
        <!-- Task List Header -->
        <div class="task-list-header">
            <div class="task-list-header-left-side">
                <i class="fa-solid fa-caret-up"></i>
                <h2 id="task-list-header-text">New Project</h2>
            </div>
            <div class="task-list-header-right-side">
                <i id="task-list-header-plus" class="fa-solid fa-plus plus-header"></i>
                <p id="task-list-header-counter">0/0</p>
                <i id="task-list-header-delete" class="fa-solid fa-xmark x-header"></i>
            </div>
        </div>

        <!-- Tasks -->
        <div id="task-list" class="task-list"></div>
    </div>
    `;

    // Append the new task container to the projects sections
    document.getElementById("projects-section").appendChild(taskContainerDiv);

    // Add event listener to the delete button of the new task and make it remove its own div when clicked
    taskContainerDiv.querySelector(".fa-xmark").addEventListener("click", function() {
        this.parentElement.parentElement.parentElement.parentElement.remove();
    });

}

// Event listener for adding a new task on click
addNewTaskContainerButton.addEventListener("click", addNewTaskContainer);

```