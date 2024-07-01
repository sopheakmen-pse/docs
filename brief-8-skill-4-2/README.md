# Project Guideline

## Steps

- Create a repository in Github
- Create a new project folder locally and add remote to your repository
- Do the project as guideline below
- Send your git repository to Trainer. Sopheak Men in discord

## Start with this HTML code

```json
<!doctype html>
<html lang="en">

<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>Todo</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet"
        integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
</head>

<body>
    <div class="container-sm mt-4">
        <div class="card">
            <div class="card-body">
                <h2 class="card-title">Todo List</h2>
                <div class="d-grid">
                    <button type="button" class="btn btn-primary" onclick="fetchTodos();">Get all todos</button>
                </div>
                <div id="loading">
                    Loading...
                </div>

                <div id="todo-list">
                    <div class="card mt-2">
                        <div class="card-body">
                            <div class="row">
                                <div class="col">ID: 1</div>
                                <div class="col">Name: Task One</div>
                                <div class="col">Status: false</div>
                            </div>
                        </div>
                    </div>
                    <div class="card mt-2">
                        <div class="card-body">
                            <div class="row">
                                <div class="col">ID: 2</div>
                                <div class="col">Name: Task Two</div>
                                <div class="col">Status: false</div>
                            </div>
                        </div>
                    </div>
                    <div class="card mt-2">
                        <div class="card-body">
                            <div class="row">
                                <div class="col">ID: 3</div>
                                <div class="col">Name: Task Three</div>
                                <div class="col">Status: false</div>
                            </div>
                        </div>
                    </div>
                </div>

            </div>
        </div>

        <div class="card mt-4">
            <div class="card-body">
                <h2 class="card-title">New Task</h2>
                <form onsubmit="createTask(event);">
                    <div class="mb-3">
                        <label for="newTask" class="form-label">Task Name</label>
                        <input type="text" placeholder="Enter a new task" class="form-control" id="newTask">
                    </div>
                    <div class="mb-3">
                        <label for="priority" class="form-label">Task Priority</label>
                        <input type="text" placeholder="Enter a priority (High, Medium, Low)" class="form-control"
                            id="priority">
                    </div>
                    <div class="mb-3">
                        <label for="createdBy" class="form-label">Created By</label>
                        <input type="text" placeholder="Enter your fullname" class="form-control" id="createdBy">
                    </div>
                    <div class="d-grid">
                        <button type="submit" class="btn btn-primary">Add a new task</button>
                    </div>
                    <p id="newTaskMessage" class="mt-2 text-center">message</p>
                </form>
            </div>
        </div>

        <div class="card mt-4">
            <div class="card-body">
                <h2 class="card-title">Complete Task</h2>
                <form>
                    <div class="mb-3">
                        <label for="completeTask" class="form-label">Task ID</label>
                        <input type="number" placeholder="Enter task ID" class="form-control" id="completeTask">
                    </div>
                    <div class="d-grid">
                        <button type="submit" class="btn btn-primary">Update the task as "done"</button>
                    </div>
                    <p id="completeTaskMessage" class="mt-2 text-center">message</p>
                </form>
            </div>
        </div>

        <div class="card my-4">
            <div class="card-body">
                <h2 class="card-title">Delete Task</h2>
                <form>
                    <div class="mb-3">
                        <label for="deleteTask" class="form-label">Task ID</label>
                        <input type="number" placeholder="Enter task ID" class="form-control" id="deleteTask">
                    </div>
                    <div class="d-grid">
                        <button type="submit" class="btn btn-danger">Delete the task</button>
                    </div>
                    <p id="deleteTaskMessage" class="mt-2 text-center">message</p>
                </form>
            </div>
        </div>
    </div>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"
        integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz"
        crossorigin="anonymous"></script>
    <!-- <script src="./index.js"></script> -->
</body>

</html>
```

## 1. Todo List

- Create an event listener when “click” to the button “Get all todos” and bind it to the function **getTodos()**
- Create a function named **getTodos()** to get all todos by **creator’s name**
    - Get data from API
    - Display data to the page (for example: innerHTML)

![Screenshot from 2024-07-01 12-00-24.png](Project%20Guideline%20b570dfd1ba8f4cef96ed394af025b423/Screenshot_from_2024-07-01_12-00-24.png)

## 2. New Task

- Create an event listener when “submit” to the form and bind it to the function **createTask(event)**
- Create a function named **createTask(event)** to post a task to API POST

![Screenshot from 2024-07-01 12-03-48.png](Project%20Guideline%20b570dfd1ba8f4cef96ed394af025b423/Screenshot_from_2024-07-01_12-03-48.png)

## 3. Complete Task

- Create an event listener when “submit” to the form and bind it to the function **completeTask(event)**
- Create a function named **completeTask(event)** to update status of the task by ID to complete via API PUT.

![Untitled](Project%20Guideline%20b570dfd1ba8f4cef96ed394af025b423/Untitled.png)

## 4. Delete Task

- Create an event listener when “submit” to the form and bind it to the function **deleteTask(event)**
- Create a function named **deleteTask(event)** to delete a task by ID from the input value, and use API DELETE.