# College Registration Form Project

## Overview

This project consists of a Django backend API and a React frontend application. The backend provides REST APIs for managing course data, while the frontend offers a user interface to interact with these APIs. Both applications are containerized using Docker and orchestrated with Docker Compose.

## Project Structure

College_registration_form_project/ ├── courses_api/ │ ├── Postgressql/ # PostgreSQL database directory │ ├── docker-compose.yml # Docker Compose configuration file │ ├── courses_api/ # Django backend code │ └── Dockerfile # Dockerfile for the Django backend └── courses-frontend/ # React frontend code └── Dockerfile # Dockerfile for the React frontend



## Prerequisites

- Docker
- Docker Compose

## Getting Started

### Clone the Repository

```bash
git clone https://github.com/your-username/your-repo-name.git
cd College_registration_form_project

Build and Start the Containers

Navigate to the courses_api directory and run the following command:

cd courses_api
docker-compose up --build

This command will build the Docker images and start the containers for both the Django backend and the PostgreSQL database.

Accessing the Application

    Backend API: The Django backend API will be accessible at http://localhost:8000.
    Frontend Application: The React frontend application will be accessible at http://localhost:3000.

Docker Compose Configuration

The docker-compose.yml file sets up the following services:

    django: The Django backend service.
    postgres: The PostgreSQL database service.

Running Migrations

If you make changes to the Django models or need to apply new migrations, you can run the following commands:

docker-compose exec django python manage.py makemigrations
docker-compose exec django python manage.py migrate

Here's the README.md content formatted for direct copy-pasting:

markdown

# College Registration Form Project

## Overview

This project consists of a Django backend API and a React frontend application. The backend provides REST APIs for managing course data, while the frontend offers a user interface to interact with these APIs. Both applications are containerized using Docker and orchestrated with Docker Compose.

## Project Structure

College_registration_form_project/ ├── courses_api/ │ ├── Postgressql/ # PostgreSQL database directory │ ├── docker-compose.yml # Docker Compose configuration file │ ├── courses_api/ # Django backend code │ └── Dockerfile # Dockerfile for the Django backend └── courses-frontend/ # React frontend code └── Dockerfile # Dockerfile for the React frontend

bash


## Prerequisites

- Docker
- Docker Compose

## Getting Started

### Clone the Repository

```bash
git clone https://github.com/your-username/your-repo-name.git
cd College_registration_form_project

Build and Start the Containers

Navigate to the courses_api directory and run the following command:

bash

cd courses_api
docker-compose up --build

This command will build the Docker images and start the containers for both the Django backend and the PostgreSQL database.
Accessing the Application

    Backend API: The Django backend API will be accessible at http://localhost:8000.
    Frontend Application: The React frontend application will be accessible at http://localhost:3000.



Running PostgreSQL

The PostgreSQL database is managed by Docker Compose. It will be available at localhost:5432 by default. Ensure that your Django settings are configured to connect to this database. The connection details are defined in your docker-compose.yml file.

docker pull postgres:15
docker-compose exec postgres psql -U your-postgres-user -d your-database
docker run --name your-postgres-container -e POSTGRES_DB=your-database -e POSTGRES_USER=your-postgres-user -e POSTGRES_PASSWORD=your-password -p 5432:5432 -d postgres:15
docker exec -it your-postgres-container psql -U your-postgres-user -d your-database



Docker Compose Configuration

The docker-compose.yml file sets up the following services:

    django: The Django backend service.
    postgres: The PostgreSQL database service.

Running Migrations

If you make changes to the Django models or need to apply new migrations, you can run the following commands:

bash

docker-compose exec django python manage.py makemigrations
docker-compose exec django python manage.py migrate

Stopping the Application

To stop the running containers, use:

docker-compose down

License

This project is licensed under the MIT License - see the LICENSE file for details.


Feel free to adjust the placeholders and details according to your project's specifics.

