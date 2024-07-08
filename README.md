# Full-Stack FastAPI and React Template

Welcome to the Full-Stack FastAPI and React template repository. This repository serves as a demo application for interns, showcasing how to set up and run a full-stack application with a FastAPI backend and a ReactJS frontend using ChakraUI.

## Project Structure

The repository is organized into two main directories:

- **frontend**: Contains the ReactJS application.
- **backend**: Contains the FastAPI application and PostgreSQL database integration.

Each directory has its own README file with detailed instructions specific to that part of the application.

## Getting Started

To get started with this template, please follow the instructions in the respective directories:

- [Frontend README](./frontend/README.md)
- [Backend README](./backend/README.md)

This is a full stack web application consisting of a React frontend and a FastAPI backend. The backend interacts with a PostgreSQL database and provides RESTful APIs for the frontend to consume.

Table of Contents
Features
Demo
Installation
Usage
Configuration
API Endpoints
Docker
Database
Contributing
License
Contact
Features
Frontend (React)

User interface for interacting with the backend services
Responsive design
Authentication forms
Backend (FastAPI)

User authentication and authorization
CRUD operations for items
JWT token-based authentication
Email notifications
Swagger and ReDoc API documentation
Demo
A live demo of the application can be found here.

Installation
Frontend
Clone the repository:

git clone https://github.com/yourusername/your-frontend-repo.git
cd your-frontend-repo
Install dependencies:

npm install
Backend
Clone the repository:

git clone https://github.com/yourusername/your-backend-repo.git
cd your-backend-repo
Install dependencies using Poetry:

poetry install

Usage
Frontend
To start the React development server:

bash
Copy code
npm start
Backend
To run the FastAPI server:

bash
Copy code
poetry run uvicorn app.main:app --reload
Configuration
Create a .env file in the root directory of the backend project and add the following environment variables:

env
Copy code
# Domain
DOMAIN=localhost

# Environment
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
POST /api/v1/login/access-token: Obtain a JWT token.
POST /api/v1/users/: Create a new user.
GET /api/v1/users/me: Get current user details.
POST /api/v1/items/: Create a new item.
GET /api/v1/items/: List all items.
Docker
Building and Running with Docker
Build the Docker images:

docker-compose build
Run the Docker containers:

docker-compose up
Database
Ensure PostgreSQL is running and accessible with the credentials provided in the .env file. Apply database migrations using Alembic:

poetry run alembic upgrade head
