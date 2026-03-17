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
├── src/
├── k8s/
│   ├── deployment.yaml
│   └── service.yaml
├── Dockerfile
├── Jenkinsfile
├── pom.xml
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
![Application Running](screenshots/ApplicationRunning.png)

### 🐳 Docker Execution
![Docker Execution](screenshots/DockerExecution.png)

### ⚙️ Jenkins Pipeline
![Jenkins Pipeline](screenshots/JenkinsPipeline.png)
---

## 📌 What I Learned

- Docker containerization
- Jenkins CI/CD basics
- YAML configuration
- End-to-end DevOps workflow

---
