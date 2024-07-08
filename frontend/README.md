# Frontend - ReactJS with ChakraUI

This directory contains the frontend of the application built with ReactJS and ChakraUI.

## Prerequisites

- Node.js (version 14.x or higher)
- npm (version 6.x or higher)

## Setup Instructions

1. **Navigate to the frontend directory**:
    ```sh
    cd frontend
    ```

2. **Install dependencies**:
    ```sh
    npm install
    ```

3. **Run the development server**:
    ```sh
    npm run dev
    ```

4. **Configure API URL**:
   Ensure the API URL is correctly set in the `.env` file.

Frontend Application
Overview
This is the frontend application for the Full Stack FastAPI Project. The frontend is built with React and interacts with the FastAPI backend to provide a seamless user experience.

Table of Contents
Overview
Features
Demo
Installation
Usage
Configuration
Scripts
Docker
Features
User authentication and authorization
CRUD operations for items
Responsive design
Integration with FastAPI backend
Error handling and notifications

Installation
To get started with the project, clone the repository and install the dependencies.
- git clone https://github.com/bakare-rasheed/devops-stage-2.git
- npm start
Configuration
Create a .env file in the root directory of the project and add the following environment variables:


REACT_APP_API_URL=http://localhost:8000/api/v1
Replace http://localhost:8000/api/v1 with the URL of your backend API.

Scripts
Here are some useful scripts for development and production:

npm start: Runs the app in development mode.
npm run build: Builds the app for production.
npm test: Runs the test suite.
npm run lint: Lints the codebase.
Docker
To build and run the application using Docker, follow these steps:

Build the Docker image:


Build the Docker image
docker build -t frontend-app .
Run the Docker container:

docker run -p 3000:80 frontend-app
This will start the application on http://localhost:3000.
