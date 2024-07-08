# Backend - FastAPI with PostgreSQL

This directory contains the backend of the application built with FastAPI and a PostgreSQL database.

## Prerequisites

- Python 3.8 or higher
- Poetry (for dependency management)
- PostgreSQL (ensure the database server is running)

### Installing Poetry

To install Poetry, follow these steps:

```sh
curl -sSL https://install.python-poetry.org | python3 -
```

Add Poetry to your PATH (if not automatically added):

## Setup Instructions

1. **Navigate to the backend directory**:
    ```sh
    cd backend
    ```

2. **Install dependencies using Poetry**:
    ```sh
    poetry install
    ```

3. **Set up the database with the necessary tables**:
    ```sh
    poetry run bash ./prestart.sh
    ```

4. **Run the backend server**:
    ```sh
    poetry run uvicorn app.main:app --reload
    ```

5. **Update configuration**:
   Ensure you update the necessary configurations in the `.env` file, particularly the database configuration.


Configuration
Create a .env file in the root directory of the project and add the following environment variables:

# Domain
DOMAIN=localhost

# Environment: local, staging, production
ENVIRONMENT=local

PROJECT_NAME="Full Stack FastAPI Project"
STACK_NAME=full-stack-fastapi-project

# Backend
BACKEND_CORS_ORIGINS="http://localhost,http://localhost:5173,https://localhost,https://localhost:5173"
SECRET_KEY=changethis123
FIRST_SUPERUSER=devops@hng.tech
FIRST_SUPERUSER_PASSWORD=devops#HNG11
USERS_OPEN_REGISTRATION=True

# Emails
SMTP_HOST=
SMTP_USER=
SMTP_PASSWORD=
EMAILS_FROM_EMAIL=info@example.com
SMTP_TLS=True
SMTP_SSL=False
SMTP_PORT=587

# Postgres
POSTGRES_SERVER=localhost
POSTGRES_PORT=5432
POSTGRES_DB=mydatabase
POSTGRES_USER=bakare
POSTGRES_PASSWORD=abiola
DATABASE_URL=postgresql://bakare:abiola@localhost:5432/mydatabase

API Endpoints
The API documentation is available at /docs for Swagger and /redoc for ReDoc once the server is running. Here are some of the main endpoints:

POST /api/v1/login/access-token: Obtain a JWT token.
POST /api/v1/users/: Create a new user.
GET /api/v1/users/me: Get current user details.
POST /api/v1/items/: Create a new item.
GET /api/v1/items/: List all items.
Docker
To build and run the application using Docker, follow these steps:

Build the Docker image:

docker build -t backend-app .
Run the Docker container:

docker run -p 8000:8000 --env-file .env backend-app
This will start the application on http://localhost:8000.

Database
Ensure that PostgreSQL is running and accessible with the credentials provided in the .env file. To apply database migrations, use Alembic:

poetry run alembic upgrade head