# 🎲 Boardgame Application

A simple web application that displays a list of popular board games.  
This project was built to practice and demonstrate a complete DevOps workflow — from development to deployment.

---

##  Overview

The goal of this project was to understand how an application moves through different stages in DevOps.

It includes:
- Building a backend application
- Containerizing it using Docker
- Automating the process with Jenkins
- Managing deployment using YAML configuration files

---

##  Tech Stack

- Java / Spring Boot
- Maven
- Docker
- Jenkins
- Git & GitHub
- YAML (Deployment & Service configuration)

---
## 📂 Project Structure
.
├── src/ # Application source code
├── Dockerfile # Docker configuration
├── Jenkinsfile # CI/CD pipeline
├── deployment.yml # Deployment setup
├── service.yml # Service configuration
├── pom.xml # Project dependencies
└── README.md


---

##  Docker Setup

### Build the image
```bash
docker build -t boardgame-app .


---

## ⚙️ CI/CD Pipeline

Jenkins is used to automate:
- Build using Maven
- Docker image creation
- Application deployment

Pipeline is defined in the `Jenkinsfile`.

---

## 📸 Screenshots

### 🌐 Application Running
![Application Running](screenshots/Application%20Running.png)

### 🐳 Docker Execution
![Docker Execution](screenshots/Docker%20Execution.png)

### ⚙️ Jenkins Pipeline
![Jenkins Pipeline](screenshots/Jenkins%20Pipeline.png)
---

## 📌 What I Learned

- Docker containerization
- Jenkins CI/CD basics
- YAML configuration
- End-to-end DevOps workflow

---
