# Contributing to Task Management System

Welcome to the Task Management System project! This project is built to manage team-based tasks efficiently through an intuitive admin dashboard, role-based access, and a task board system.

This document outlines contribution practices and highlights the initial commit, which established a foundational system for **task creation, user retrieval, and task visualization** via backend APIs and frontend layout.

---

## First Contribution Overview

### Author: Viren Bhadiyadra 
### Commit Message: `Initial commit – Add task creation & retrieval APIs, responsive UI`

---

##  Objective of Initial Commit

This commit establishes the base functionality and interface for the Task Management System. It includes:

### 💻 Backend Development:
1. **`create_task.php`**
   - Enables task creation through POST method.
   - Inputs are validated and inserted into the `tasks` table.
   - Tracks `created_by` using session.

2. **`get_tasks.php`**
   - Retrieves all tasks along with assigned users.
   - Performs a `LEFT JOIN` to get usernames and roles.

3. **`get_users_for_task.php`**
   - Retrieves all users eligible for task assignment (`user`, `team-lead` roles only).

---

### Frontend UI Enhancements:

- Created a **responsive admin dashboard** using `flex` and `grid` layouts.
- Includes sections for:
  - Task creation form
  - Task board (`kanban-style`)
- Styled using:
  - `linear-gradient` backgrounds
  - Card-like components
  - Hover effects
  - Media queries for mobile responsiveness

---

##  Authentication

- `create_task.php` relies on a session (`$_SESSION['admin_id']`) to associate the task with the creator.
- Ensure session management is configured and active across all backend pages requiring authentication.

---

## Technologies Used

| Stack          | Description                         |
|----------------|-------------------------------------|
| PHP            | Backend API scripting               |
| MySQL          | Database for users and tasks        |
| HTML/CSS       | UI structure and design             |
| JavaScript     | (Expected in next phases) for dynamic interactivity |
| Flexbox/Grid   | Layout styling for responsive UI    |

---

## Project Structure (so far)

```text
project-root/
│
├── backend/
│   ├── create_task.php
│   ├── get_tasks.php
│   └── get_users_for_task.php
│
├── styles/
│   └── main.css (UI styling for landing, login, dashboard)
│
├── index.html
├── login.html
├── dashboard.html
└── README.md

```

---

## Second Contribution Overview

### Commit Message: `Add task status update API endpoint`

---

### Purpose

This update introduces a backend API endpoint that allows the **task status** (e.g., "To Do", "In Progress", "Done") to be updated dynamically from the frontend. This is an essential part of the **Kanban-style task board**, enabling drag-and-drop updates or button-triggered transitions.

---

### 💻 File Added/Updated

#### ➕ `update_task_status.php`

**Description:**  
- Accepts a `POST` request with:
  - `task_id`: ID of the task to update
  - `status`: New status to be assigned
- Validates input
- Uses `prepared statements` for safe SQL execution
- Responds with a JSON object indicating success or failure

**Code Overview:**
```php
if ($_SERVER["REQUEST_METHOD"] === "POST") {
    $taskId = $_POST['task_id'] ?? null;
    $newStatus = $_POST['status'] ?? null;

    if (!$taskId || !$newStatus) {
        echo json_encode(["success" => false, "message" => "Missing task_id or status"]);
        exit;
    }

    $conn = Database::getInstance()->getConnection();
    $stmt = $conn->prepare("UPDATE tasks SET status = ? WHERE id = ?");
    $stmt->bind_param("si", $newStatus, $taskId);

    if ($stmt->execute()) {
        echo json_encode(["success" => true, "message" => "Task status updated"]);
    } else {
        echo json_encode(["success" => false, "message" => "Update failed"]);
    }
}

```

---

## Third Contribution Overview

### Commit Message: `Add user dashboard with drag-and-drop Kanban task board`

---

### Purpose

This commit introduces a fully functional **User Dashboard** featuring a **Kanban-style task board** where users can visually manage their assigned tasks. It enables users to:

- View tasks grouped by status: "To Do", "In Progress", "Completed"
- Drag and drop tasks across columns
- Automatically update task status through an AJAX-powered backend call
- Receive toast notifications for successful status changes
- Sign out using a styled button

---

### 📁 Files Added/Updated

####  `user/dashboard.html`
- A structured HTML page containing:
  - Page title and sign-out button
  - A responsive Kanban board with three columns for task status
  - Containers for task cards
  - Toast notification container for success feedback

#### `user/user.js`
- JavaScript logic that:
  - Fetches and renders user-specific tasks
  - Groups tasks based on `status` and sorts by priority (`high > medium > low`)
  - Enables **drag-and-drop interaction**
  - Sends task status updates to the backend (`updateTaskStatus.php`) using `fetch()`
  - Handles visual feedback using a toast notification (`notifyUser()`)

---

### Key Features

| Feature               | Description                                                                 |
|------------------------|-----------------------------------------------------------------------------|
| Drag-and-Drop UI       | Enables moving tasks across columns using standard HTML5 drag events        |
| Auto Refresh on Drop   | Reloads board after a task is moved to reflect updated status               |
| Backend Integration    | Communicates with `updateTaskStatus.php` to persist changes                 |
| Priority Sorting       | Tasks are sorted inside each column based on priority (high → low)          |
| Toast Notification     | Shows status updates via animated success messages                          |
| Responsive Design      | Optimized layout that stacks columns vertically on smaller devices          |

---

### Backend Integration

**Endpoint Used:**  
- `../backend/updateTaskStatus.php`

**Request Format:**
```http
POST /updateTaskStatus.php
Content-Type: application/x-www-form-urlencoded

task_id=14&status=inprogress
```

