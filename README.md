# 🚀 Multi-User Task Management API

A simple **Multi-User Task Management REST API** built using **Python and FastAPI**.

This project allows multiple users to create, view, update, complete, and delete tasks. Tasks can be assigned to specific users.

---

## 📌 Project Overview

The Multi-User Task Management API is a backend application developed with FastAPI.

Users can:

* Create users
* View users
* Create tasks
* Assign tasks to users
* View all tasks
* View tasks for a specific user
* Update tasks
* Mark tasks as completed
* Delete tasks

The project is designed to understand the fundamentals of **REST API development using FastAPI**.

---

## 🛠️ Technologies Used

* 🐍 Python
* ⚡ FastAPI
* 📦 Pydantic
* 🔗 REST API
* 📖 Swagger UI
* 🚀 Uvicorn

---

## 📂 Project Structure

```text
multi-user-task-management/
│
├── main.py
└── README.md
```

---

## ⚙️ Installation

### Step 1: Install Python

Make sure Python is installed on your computer.

Check the Python version:

```bash
python --version
```

---

### Step 2: Create Project Folder

```bash
mkdir multi-user-task-management
cd multi-user-task-management
```

---

### Step 3: Install Required Packages

```bash
pip install fastapi uvicorn
```

---

## ▶️ Run the Project

Run the following command:

```bash
uvicorn main:app --reload
```

The API will start at:

```text
http://127.0.0.1:8000
```

---

## 📖 Swagger API Documentation

FastAPI automatically provides interactive API documentation.

Open:

```text
http://127.0.0.1:8000/docs
```

You can test all API endpoints directly from Swagger UI.

---

## 🔗 API Endpoints

### 🏠 Home

```http
GET /
```

Returns a message confirming that the API is running.

---

### 👤 Get All Users

```http
GET /users
```

Returns all users.

---

### 👤 Get User

```http
GET /users/{user_id}
```

Example:

```http
GET /users/1
```

---

### ➕ Create User

```http
POST /users
```

Request body:

```json
{
  "id": 4,
  "name": "Ravi",
  "email": "ravi@gmail.com"
}
```

---

### 📋 Get All Tasks

```http
GET /tasks
```

Returns all tasks.

---

### 👤📋 Get Tasks of a User

```http
GET /users/{user_id}/tasks
```

Example:

```http
GET /users/1/tasks
```

This returns only the tasks assigned to user `1`.

---

### ➕ Create Task

```http
POST /tasks
```

Request body:

```json
{
  "title": "Learn FastAPI",
  "description": "Practice FastAPI REST API development",
  "user_id": 1
}
```

---

### 🔍 Get One Task

```http
GET /tasks/{task_id}
```

Example:

```http
GET /tasks/1
```

---

### ✏️ Update Task

```http
PUT /tasks/{task_id}
```

Example:

```http
PUT /tasks/1
```

Request body:

```json
{
  "title": "Learn Python and FastAPI",
  "description": "Complete FastAPI practice project",
  "user_id": 1
}
```

---

### ✅ Complete Task

```http
PATCH /tasks/{task_id}/complete
```

Example:

```http
PATCH /tasks/1/complete
```

The task status will change to:

```json
{
  "completed": true
}
```

---

### 🗑️ Delete Task

```http
DELETE /tasks/{task_id}
```

Example:

```http
DELETE /tasks/1
```

---

## 📊 Example Users

The project starts with sample users:

| ID | Name  | Email                                     |
| -: | ----- | ----------------------------------------- |
|  1 | Rahul | [rahul@gmail.com](mailto:rahul@gmail.com) |
|  2 | Kiran | [kiran@gmail.com](mailto:kiran@gmail.com) |
|  3 | Anil  | [anil@gmail.com](mailto:anil@gmail.com)   |

---

## 📝 Example Task

```json
{
  "id": 1,
  "title": "Learn Python",
  "description": "Practice Python basics",
  "completed": false,
  "user_id": 1
}
```

Here, the task is assigned to **User ID 1**.

---

## 🔄 CRUD Operations

This project demonstrates CRUD operations:

| Operation | HTTP Method | Endpoint           |
| --------- | ----------- | ------------------ |
| Create    | POST        | `/tasks`           |
| Read      | GET         | `/tasks`           |
| Update    | PUT         | `/tasks/{task_id}` |
| Delete    | DELETE      | `/tasks/{task_id}` |

It also includes a separate endpoint for completing tasks.

---

## 🎯 Learning Objectives

Through this project, I learned:

* How to create a FastAPI application
* How REST APIs work
* HTTP methods
* GET, POST, PUT, PATCH, and DELETE
* Pydantic models
* Request validation
* Path parameters
* CRUD operations
* User-task relationships
* Exception handling
* Swagger API documentation
* Running APIs with Uvicorn

---

## 🚀 Future Improvements

The current version uses an in-memory list for storing users and tasks.

Future improvements could include:

* 🗄️ SQLite/MySQL/PostgreSQL database
* 🔐 JWT authentication
* 👤 User login and registration
* 🔑 Password hashing
* 🛡️ User authorization
* 📅 Task deadlines
* ⭐ Task priorities
* 🔎 Task search and filtering
* 📊 Task statistics
* 🐳 Docker deployment
* ☁️ Cloud deployment



This project is created for learning and educational purposes.
