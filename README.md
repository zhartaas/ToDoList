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
