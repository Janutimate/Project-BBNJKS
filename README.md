# Student Attendance Management System (Dockerised)

This application is a full-stack student attendance management system.  
It has been fully containerised using **Docker** and **Docker Compose** to allow it to run end-to-end in a clean environment.

---

## How to Run the Application (Docker)

The application runs entirely inside Docker containers. No local installation of Node.js or MongoDB is required.

---

## Prerequisites

- Docker Desktop installed and running  
  https://www.docker.com/products/docker-desktop/

---

## Setup Instructions

1. **Clone the repository**
   ```bash
   git clone <your-repository-url>
   cd Project-BBNJKS


2. **Create the environment configuration**

In the backend directory, create a .env file using the example provided:

backend/.env.example → backend/.env


The .env file should contain:

PORT=5000
MONGO_URI=mongodb://mongo:27017/qr_attendance


3. **Build and start the application**

From the project root directory, run:

docker-compose up --build


This will:
   -Build and start the backend (Node.js + Express)
   -Build and start the frontend (served via Nginx)
   -Start a MongoDB database container
   -Connect all services together

4. **Accessing the Application**

Frontend (Web Application):
http://localhost:3000

Backend API:
http://localhost:5000

5. **Student Identification**

To uniquely identify this individual submission, the backend will show the following endpoint:

Endpoint:
GET /api/student

URL:
http://localhost:5000/api/student


Response (JSON):
{
  "name": "januth Aditha Abeysinghe",
  "studentId": "225644509"
}

This endpoint is accessible from the Dockerised version of the application.


6. **Stopping the Application**

To stop all running containers, press:

CTRL + C

Or run:

docker-compose down