# Todo List App with FastAPI

A complete todo list application with a modern web interface and REST API built with FastAPI.

## Features

### Backend API
- Create, read, update, and delete todos
- Mark todos as completed or pending
- Filter todos by completion status
- Automatic API documentation with Swagger UI
- RESTful API endpoints

### Frontend Interface
- Modern, responsive web interface
- Interactive todo management
- Real-time statistics
- Filter todos by status (All, Pending, Completed)
- Edit and delete todos with confirmation
- Beautiful gradient design with animations
- Mobile-friendly responsive layout

## Setup

1. Activate the virtual environment:
   ```bash
   source venv/bin/activate
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the application:
   ```bash
   python main.py
   ```

   Or alternatively:
   ```bash
   uvicorn main:app --reload
   ```

## API Endpoints

- `GET /` - Welcome message
- `GET /todos` - Get all todos
- `GET /todos/{todo_id}` - Get a specific todo
- `POST /todos` - Create a new todo
- `PUT /todos/{todo_id}` - Update a todo
- `DELETE /todos/{todo_id}` - Delete a todo
- `GET /todos/completed` - Get completed todos
- `GET /todos/pending` - Get pending todos

## Access the Application

Once the server is running, visit:
- **Web Interface**: http://localhost:8000 (Main todo list interface)
- **API Documentation**: http://localhost:8000/docs (Swagger UI)
- **Alternative API Docs**: http://localhost:8000/redoc

## Example Usage

Create a new todo:
```bash
curl -X POST "http://localhost:8000/todos" \
     -H "Content-Type: application/json" \
     -d '{"title": "Learn FastAPI", "description": "Build a todo API", "completed": false}'
```

Get all todos:
```bash
curl -X GET "http://localhost:8000/todos"
```
