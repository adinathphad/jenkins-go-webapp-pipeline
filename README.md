# Jenkins CI/CD Pipeline for Go Web Application

This project demonstrates a simple **CI/CD pipeline using Jenkins and Docker**.

The pipeline automatically:

- Pulls code from GitHub
- Runs Go tests
- Builds a Docker image
- Deploys the application

---

# Project Architecture

Developer pushes code -> GitHub Repository -> Jenkins Pipeline -> Run Tests -> Build Docker Image -> Deploy Container -> Application Running

---

# Technologies Used

- Jenkins
- Docker
- Go (Golang)
- GitHub

---

# Pipeline Stages

## Clone Repository

Jenkins pulls source code from GitHub.
