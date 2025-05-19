# FastAPI Template

A modern, production-ready FastAPI template with SQLAlchemy, Pydantic, and best practices.

## Features

- FastAPI framework with modern Python type hints
- SQLAlchemy ORM with async support
- Pydantic v2 for data validation
- CORS middleware
- Environment-based configuration
- SQLite database (can be easily changed to PostgreSQL)
- CRUD operations example
- API versioning
- OpenAPI documentation

## Setup

1. Create a virtual environment:
```bash
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Run the application:
```bash
uvicorn app.main:app --reload
```

## API Documentation

Once the application is running, you can access:
- Swagger UI: http://127.0.0.1:8000/docs
- ReDoc: http://127.0.0.1:8000/redoc

## Project Structure

```
app/
├── api/
│   ├── v1/
│   │   ├── endpoints/
│   │   │   └── items.py
│   │   └── api.py
├── core/
│   ├── config.py
│   └── security.py
├── db/
│   └── base.py
├── models/
│   └── item.py
├── schemas/
│   └── item.py
└── main.py
```

## API Endpoints

- `GET /api/v1/items/` - List all items
- `POST /api/v1/items/` - Create a new item
- `GET /api/v1/items/{item_id}` - Get a specific item
- `PUT /api/v1/items/{item_id}` - Update an item
- `DELETE /api/v1/items/{item_id}` - Delete an item
