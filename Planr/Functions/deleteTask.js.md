# deleteTask.js
### Goal
With the plus icon in *Planr*, one can create a new task. Similarly, one needs to be able to delete a task when clicking the associated x icon.

### Prerequisites
Inside the task-container.html there is a div element with a class of "task-list".  Inside this div element, more div elements with the class of "task" will be present. There needs to be a way to delete each individual task div.

```js
<!-- Tasks -->
<div class="task-list">
    <div class="task">
        <i class="fa-regular fa-circle task-icon-incomplete"></i>
        <div class="task-text" contenteditable="true"></div>
        <i id="task-delete" class="fa-solid fa-xmark" onclick="deleteTask()"></i>
    </div>
</div>
```
### Pseudocode
1. Find the task div that the x button is inside of and give it a variable.
2. Un-append this div from the "task-list" container.

### Code

```js
```

To add a task, see [[addNewTask.js]]