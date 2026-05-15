# Docker-Based Multi-Container Full Stack Application

## 📌 Project Overview

This project is an advanced Docker-based multi-container application developed after completing 25 days of DevOps training. The application demonstrates how frontend, backend, and database services can run independently inside separate Docker containers while communicating seamlessly with each other.

The project follows a full-stack architecture using:

* Frontend: Nginx + HTML
* Backend: Python Flask API
* Database: MySQL
* Containerization: Docker
* Orchestration: Docker Compose

The main objective of this project is to understand containerization, service communication, reverse proxy setup, networking, and persistent storage using Docker technologies.

---

# 🚀 Technologies Used

## 🐳 DevOps & Containerization

* Docker
* Docker Compose
* Docker Networking
* Docker Volumes
* Nginx Reverse Proxy

## 💻 Backend

* Python
* Flask
* REST API

## 🗄️ Database

* MySQL

## 🌐 Frontend

* HTML
* CSS
* JavaScript
* Nginx

---

# 🧠 System Architecture

The system follows a multi-container architecture where each service runs independently.

```text
User
   ↓
Frontend Container (Nginx)
   ↓
Backend Container (Flask API)
   ↓
Database Container (MySQL)
```

## 🔹 Architecture Explanation

### Frontend Container

* Hosts the user interface.
* Built using HTML pages.
* Served using Nginx.
* Sends API requests to the backend.

### Backend Container

* Built using Flask.
* Processes user requests.
* Handles API routes.
* Connects with MySQL database.

### Database Container

* Stores application data.
* Uses MySQL database.
* Data persistence handled using Docker volumes.

### Docker Network

* All containers communicate using Docker internal networking.
* Containers can access each other using service names.

### Nginx Reverse Proxy

* Nginx acts as a reverse proxy.
* Forwards frontend API requests to Flask backend.

---

# 🔁 Project Workflow

## Step 1 — User Interaction

The user opens the frontend application and fills out the form.

## Step 2 — Frontend Request

The frontend sends the request to:

```text
/api/submit
```

## Step 3 — Reverse Proxy Routing

Nginx receives the request and forwards it to the Flask backend container.

## Step 4 — Backend Processing

The Flask backend:

* Receives user data
* Validates request
* Connects with MySQL database
* Stores the information

## Step 5 — Database Storage

The MySQL container stores the data permanently.

## Step 6 — Fetching Data

The frontend requests stored records using:

```text
/api/students
```

## Step 7 — Displaying Results

The backend fetches data from MySQL and returns it to the frontend.

The frontend then displays the data on the UI.

---

# 🐳 Docker Concepts Used

## 📦 Dockerfile

Dockerfiles are used to build custom images for:

* Frontend container
* Backend container

They define:

* Base image
* Dependencies
* Working directory
* Startup commands

---

## ⚙️ Docker Compose

Docker Compose is used to manage multiple containers together.

It helps:

* Start all services together
* Define networking
* Configure volumes
* Manage dependencies

Command used:

```bash
docker-compose up --build
```

---

## 🌐 Docker Network

Docker networking allows containers to communicate internally.

Benefits:

* Service isolation
* Easy communication
* Secure internal traffic

---

## 💾 Docker Volumes

Docker volumes are used for persistent data storage.

Benefits:

* Data remains safe even if containers stop
* Database persistence
* Easy backup and management

---

# 📂 Project Structure

```text
DevOps_Project/
│
├── backend/
│   ├── app.py
│   └── dockerfile
│
├── frontend/
│   ├── login.html
│   ├── view.html
│   ├── default.conf
│   └── dockerfile
│
├── docker-compose.yml
│
└── .vscode/
```

---

# ⚙️ Setup & Installation

## Step 1 — Clone Repository

```bash
git clone <your-repository-link>
cd Project-2_devops
```

---

## Step 2 — Start Docker

Make sure Docker Desktop is running.

---

## Step 3 — Build and Run Containers

```bash
docker-compose up --build
```

---

## Step 4 — Access Application

Frontend:

```text
http://localhost
```

Backend API:

```text
http://localhost/api
```

---


# 🎯 Features

✅ Multi-container architecture
✅ Frontend-backend communication
✅ Reverse proxy using Nginx
✅ REST API integration
✅ MySQL database connectivity
✅ Persistent storage using volumes
✅ Docker Compose orchestration
✅ Container networking
✅ Modular deployment

---

# 📚 Learning Outcomes

Through this project, the following DevOps concepts were learned:

* Containerization
* Docker image creation
* Multi-container deployment
* Docker Compose orchestration
* Reverse proxy configuration
* Service communication
* Persistent data management
* Backend API integration
* DevOps workflow basics

---

# 🚀 Future Improvements

Possible future enhancements:

* User authentication
* Kubernetes deployment
* CI/CD pipeline integration
* HTTPS support
* Monitoring using Prometheus & Grafana
* Cloud deployment using AWS
* Load balancing
* Jenkins automation

---

# 🏁 Conclusion

This project successfully demonstrates containerization, service communication, and data persistence using Docker.

By separating the frontend, backend, and database into independent containers, the system becomes:

* Modular
* Scalable
* Portable
* Easy to deploy
* Easier to maintain

The project also provides practical exposure to real-world DevOps concepts including Docker networking, reverse proxy configuration, container orchestration, and persistent storage management.

---

