# Student Performance Prediction - Deployment

This repository contains the Docker Compose configuration required to deploy the Student Performance Prediction System.

## Architecture

```text
Browser
   |
   v
Frontend (Next.js)
   |
   v
Backend (FastAPI)
   |
   v
MySQL Database
```

The frontend and backend are deployed using pre-built Docker images hosted on Docker Hub.

---

## Prerequisites

Before starting the application, ensure:

* Docker Desktop is installed and running.
* MySQL Server is accessible.
* Database credentials are available.

---

## Project Structure

```text
student-performance-deployment/
│
├── docker-compose.yml
├── .env
├── .env.example
└── README.md
```

---

## Environment Variables

Create a `.env` file in the root directory.

Example:

```env
DB_PASSWORD=your_mysql_password
SECRET_KEY=your_secret_key
```

Example:

```env
DB_PASSWORD=Sagar@1234
SECRET_KEY=mysecret
```

---

## Start Application

Run:

```bash
docker compose up -d
```

Docker Compose will:

* Pull Backend Image
* Pull Frontend Image
* Create Required Containers
* Start Services

---

## Verify Containers

```bash
docker ps
```

Expected Containers:

```text
student-performance-api
student-performance-ui
```

---

## Application URLs

Frontend:

```text
http://localhost:3000
```

Backend:

```text
http://localhost:8000
```

Swagger Documentation:

```text
http://localhost:8000/docs
```

---

## View Logs

View all logs:

```bash
docker compose logs -f
```

Backend logs:

```bash
docker logs student-performance-api
```

Frontend logs:

```bash
docker logs student-performance-ui
```

---

## Stop Application

```bash
docker compose down
```

---

## Restart Application

```bash
docker compose restart
```

---

## Pull Latest Images

If newer versions are published to Docker Hub:

```bash
docker compose pull
docker compose up -d
```

---

## Troubleshooting

### Verify Docker

```bash
docker --version
docker compose version
```

### Verify Running Containers

```bash
docker ps
```

### Check Container Logs

```bash
docker compose logs -f
```

### Validate Docker Compose Configuration

```bash
docker compose config
```

---

## Technology Stack

* Next.js
* FastAPI
* MySQL
* Docker
* Docker Compose

---

## Author

Sagar Kumar
