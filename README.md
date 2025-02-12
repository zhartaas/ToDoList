# ToDo List API

## Overview

The ToDo List API is a simple task management system that allows users to create, update, delete, and retrieve tasks efficiently. The API is designed to help users manage their to-do lists by tracking tasks based on their statuses (active or done).

## Table of Contents

- [API Endpoints](#api-endpoints)
  - [Create Task](#create-task)
  - [Delete Task](#delete-task)
  - [Get Tasks](#get-tasks)
  - [Mark Task as Done](#mark-task-as-done)
  - [Update Task](#update-task)
- [Data Models](#data-models)
  - [Task](#task)
  - [Task Input](#task-input)
  - [Task Response](#task-response)
- [Error Handling](#error-handling)
- [Usage](#usage)
- [License](#license)

## API Endpoints

### Create Task

- **Endpoint**: `POST /create`
- **Description**: Creates a new task with a title and a due date.
- **Request Body**:
  ```json
  {
    "title": "Прочитать книгу",
    "activeAt": "2026-01-02"
  }

## Responses

- **200 OK** - Task successfully created.
- **404 Not Found** - Client error.
- **500 Internal Server Error** - Server-side error.

---

## Delete Task

- **Endpoint**: `DELETE /delete`
- **Description**: Deletes a task by its ID.
- **Query Parameters**:
  - `id` (string, required) - The ID of the task to delete.
- **Responses**:
  - **204 No Content** - Task successfully deleted.
  - **404 Not Found** - Task not found.
  - **500 Internal Server Error** - Server-side error.

---

## Get Tasks

- **Endpoint**: `GET /getTasks`
- **Description**: Retrieves tasks based on their status (active or done).
- **Query Parameters**:
  - `status` (string, optional) - Filter tasks by status (active or done).
- **Responses**:
  - **200 OK** - Returns an array of tasks.
  - **404 Not Found** - No tasks found.
  - **500 Internal Server Error** - Server-side error.

---

## Mark Task as Done

- **Endpoint**: `PUT /taskDone`
- **Description**: Marks a task as completed by its ID.
- **Query Parameters**:
  - `id` (string, required) - The ID of the task to mark as done.
- **Responses**:
  - **204 No Content** - Task successfully marked as done.
  - **404 Not Found** - Task not found.
  - **500 Internal Server Error** - Server-side error.

---

## Update Task

- **Endpoint**: `PUT /update`
- **Description**: Updates an existing task by its ID.
- **Query Parameters**:
  - `id` (string, required) - The ID of the task to update.
- **Request Body**:
  ```json
  {
    "title": "Обновленное название задачи",
    "activeAt": "2026-02-15"
  }
  ## Responses

- **200 OK** - Task successfully updated.
- **404 Not Found** - Task not found.
- **500 Internal Server Error** - Server-side error.

---

## Data Models

### Task

```json
{
  "id": "12345",
  "title": "Прочитать книгу",
  "activeAt": "2026-01-02"
}

## Task Response

```json
{
  "id": "12345"
}

