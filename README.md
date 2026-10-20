# Task Manager REST API

A RESTful API built with Python and FastAPI to manage tasks through standard HTTP methods.

## Features

- Create tasks with a title, description, and completion status
- Retrieve all tasks or a task by ID
- Update task completion status
- Delete tasks
- Validate request data using Pydantic
- Handle missing tasks with HTTP 404 responses
- Explore endpoints using interactive Swagger UI documentation

## Tech Stack

- Python
- FastAPI
- Pydantic
- REST APIs and HTTP methods
- Uvicorn
- Git and GitHub

## Run Locally

### 1. Clone the repository

Replace `YOUR_GITHUB_USERNAME` with your GitHub username.

```bash
git clone https://github.com/Pragatisheel-342/task-manager-api.git
cd task-manager-api
```

### 2. Create and activate a virtual environment

For Windows PowerShell:

```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
```

### 3. Install dependencies

```powershell
pip install -r requirements.txt
```

### 4. Start the server

```powershell
python -m uvicorn main:app --reload
```

### 5. Open the API documentation

Visit http://127.0.0.1:8000/docs

## API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| GET | `/` | API health check |
| POST | `/tasks` | Create a task |
| GET | `/tasks` | List all tasks |
| GET | `/tasks/{task_id}` | Retrieve one task |
| PATCH | `/tasks/{task_id}` | Update completion status |
| DELETE | `/tasks/{task_id}` | Delete a task |

## Current Limitations

Tasks are stored in memory and are cleared when the server restarts. Database persistence, authentication, and automated tests are not implemented yet.

## Future Improvements

- PostgreSQL persistence
- Automated testing with pytest
- Authentication and authorization
- Deployment to a hosting platform