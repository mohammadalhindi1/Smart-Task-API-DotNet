# Smart Task API (.NET)

A clean and scalable **RESTful Task Management API** built using **ASP.NET Core Web API**.  
This project demonstrates backend fundamentals, clean architecture principles, and how to expose business logic as reusable services.

---

## Project Overview

Smart Task API provides a set of REST endpoints to manage tasks with priorities, statuses, and deadlines.  
The API is designed with a clean structure that separates concerns and can easily be extended with authentication, persistence, or cloud deployment.

This project focuses on **how real backend systems are built**, not just how to write endpoints.

---

## Features

- RESTful API design
- Full CRUD operations on tasks
- Task attributes:
  - Title & description
  - Status: `TODO`, `IN_PROGRESS`, `DONE`
  - Priority: `LOW`, `MEDIUM`, `HIGH`
  - Deadline
- Proper HTTP status codes
- Input validation and basic error handling
- In-memory data storage (easy to replace later)

---

## Concepts Demonstrated

### Backend Fundamentals
- REST architecture
- HTTP methods (GET, POST, PUT, DELETE)
- JSON serialization/deserialization
- Status codes (`200`, `201`, `400`, `404`)

### Object-Oriented Programming
- Encapsulation of business logic
- Interfaces for abstraction
- Dependency Injection (DI)
- Separation between Controllers, Services, and Repositories

### Clean Architecture
- Controllers handle HTTP concerns
- Services contain business logic
- Repositories manage data access
- Models represent domain entities

---

## 🗂️ Project Structure 

```
Controllers/
└── TasksController.cs

Models/
├── TaskItem.cs
├── TaskStatus.cs
└── Priority.cs

Services/
├── ITaskService.cs
└── TaskService.cs

Repositories/
├── ITaskRepository.cs
└── InMemoryTaskRepository.cs

Program.cs
```

---

## ▶️ How to Run

### Requirements
- .NET 8 SDK (or .NET 7)

### Run the API
```bash
dotnet restore
dotnet run
```

The API will be available at:
```
https://localhost:5001
```
Swagger UI:
```
https://localhost:5001/swagger
```

📡 API Endpoints (Examples)
Method	Endpoint	Description
GET	/api/tasks	Get all tasks
GET	/api/tasks/{id}	Get task by ID
POST	/api/tasks	Create a new task
PUT	/api/tasks/{id}	Update an existing task
DELETE	/api/tasks/{id}	Delete a task

Example Request (POST) :
```
{
  "title": "Prepare technical interview",
  "description": "Review OOP and data structures",
  "priority": "HIGH",
  "status": "TODO",
  "deadline": "2026-01-05"
}
```

Future Improvements :
Add database support (Entity Framework + SQL)
Add authentication (JWT)
Add pagination and filtering
Dockerize the API
Deploy to cloud (AWS / Azure)
Add unit and integration tests

🔗 Relation to Java Project
This API is the backend version of the Smart Task Manager (Java) project.
Java project focuses on core OOP and data structures
.NET project focuses on backend architecture and API design
Together, they demonstrate strong fundamentals across different technologies.

👨‍💻 Author
Mohammad Alhindi : Cloud Computing | Backend / Software Engineer

GitHub: https://github.com/mohammadalhindi1

LinkedIn: www.linkedin.com/in/mohammad-alhendi13
