# Smart Task API (.NET)

A clean and scalable **RESTful Task Management API** built using **ASP.NET Core Web API**.  
This project focuses on backend fundamentals and demonstrates how to structure and expose business logic through well-defined API endpoints.

---

## Project Overview

Smart Task API provides a set of REST endpoints to manage tasks with priorities, statuses, and deadlines.  
The project is structured using a clear **layered architecture** that separates concerns and makes the codebase easy to read, maintain, and extend.

This project focuses on **how real backend systems are organized**, not just how to write endpoints.

---

## Features

- RESTful API design
- Full CRUD operations on tasks
- Task attributes:
  - Title
  - Description
  - Status: `TODO`, `IN_PROGRESS`, `DONE`
  - Priority: `LOW`, `MEDIUM`, `HIGH`
  - Deadline
- Proper HTTP status codes
- Basic input validation and error handling
- In-memory data storage (easy to replace later)

---

## Concepts Demonstrated

### Backend Fundamentals
- REST architecture
- HTTP methods (GET, POST, PUT, DELETE)
- JSON serialization and deserialization
- HTTP status codes (`200`, `201`, `400`, `404`)

### Object-Oriented Programming
- Encapsulation of business logic
- Interfaces for abstraction
- Dependency Injection (DI)
- Separation between Controllers, Services, and Repositories

### Application Structure
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

Example Request (POST)

```
{
  "title": "Prepare technical interview",
  "description": "Review OOP and data structures",
  "priority": "HIGH",
  "status": "TODO",
  "deadline": "2026-01-05"
}
```

Future Improvements
The following enhancements could be added in the future:
Database support using Entity Framework and SQL
Authentication using JWT
Pagination and filtering
Dockerizing the API
Cloud deployment (AWS / Azure)
Unit and integration testing

🔗 Relation to Java Project
This API is the backend version of the Smart Task Manager (Java) project.
The Java project focuses on core OOP principles and data structures
The .NET project focuses on backend API design and layered architecture
Together, they demonstrate a solid foundation across different backend technologies.

👨‍💻 Author

Mohammad Alhindi
Cloud Computing | Backend / Software Engineer

GitHub: https://github.com/mohammadalhindi1

LinkedIn: https://www.linkedin.com/in/mohammad-alhendi13
