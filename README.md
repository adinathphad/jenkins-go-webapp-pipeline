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

git https://github.com/kodekloudhub/go-webapp-sample.git

---

## Run Tests

Runs Go unit tests.
go test ./...

---

## Build Docker Image

Build Docker image using project Dockerfile.
docker build -t adminturneddevops/go-webapp-sample .

---

## Deploy Application

Run container and expose port.
docker run -p 8090:8000 -d adminturneddevops/go-webapp-sample

Host Port → 8090  
Container Port → 8000

---

# Access Application

After deployment open:
http://<server-ip>:8090

Login:
username: test
password: test

---

# Learning Outcomes

This project demonstrates:

- Jenkins Pipeline as Code
- CI/CD workflow
- Docker container deployment
- Git integration

---

# Future Improvements

- Push Docker image to DockerHub
- Add GitHub webhook triggers
- Deploy to Kubernetes
- Add security scanning
