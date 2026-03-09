# Simple Task Manager (HTML + JavaScript)

A lightweight **static task manager application** built using plain **HTML, CSS, and JavaScript**.
This project demonstrates basic front-end functionality including task creation, deletion, completion tracking, search, and browser persistence using `localStorage`.

The project is intentionally simple and dependency-free so it can run directly in any browser.

---

## Features

* Add new tasks
* Delete tasks
* Mark tasks as completed
* Live task search
* Persistent storage using **localStorage**
* Dynamic DOM updates
* No external frameworks required

---

## How It Works

### Task Storage

Tasks are stored in the browser using `localStorage`.

Example structure:

```
[
  {
    "text": "Finish documentation",
    "completed": false
  },
  {
    "text": "Push code to GitHub",
    "completed": true
  }
]
```

When the page loads, the application reads from `localStorage` and renders the saved tasks.

---

### Main Functions

#### `addTask()`

Adds a new task to the task list.

Steps:

1. Reads text from the input field
2. Creates a task object
3. Pushes the object into the `tasks` array
4. Saves tasks to `localStorage`
5. Re-renders the task list

---

#### `deleteTask(index)`

Removes a task from the list.

Steps:

1. Removes the task using `splice()`
2. Updates `localStorage`
3. Re-renders the UI

---

#### `toggleComplete(index)`

Marks a task as complete or incomplete.

Steps:

1. Toggles the `completed` boolean
2. Saves updated tasks
3. Updates the UI styling

Completed tasks appear with a **strikethrough style**.

---

#### `searchTasks()`

Filters tasks based on the search input.

Steps:

1. Reads search text
2. Filters tasks using `Array.filter()`
3. Displays only matching results

---

## Project Structure

```
task-manager-demo
│
├── index.html
└── README.md
```

---

## Running the Project

No build step required.

Simply open the file:

```
index.html
```

in any browser.

---

## Possible Improvements

* Edit existing tasks
* Add task categories
* Add due dates
* Dark mode support
* Convert to React or Vue
* Store tasks in a backend database

---

## License

MIT License
