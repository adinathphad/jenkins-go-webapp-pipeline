# Pipeline Explanation

This Jenkins pipeline automates the build and deployment of a Go web application.

## Stage 1 — Clone Repository

Jenkins clones the application source code from GitHub.

## Stage 2 — Run Tests

The Go testing framework runs unit tests to verify the application.

## Stage 3 — Build Docker Image

Docker builds a container image containing the application.

## Stage 4 — Deploy Application

The container is started and the application becomes accessible.
