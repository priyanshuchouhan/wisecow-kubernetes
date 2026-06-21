# Wisecow Kubernetes Deployment

## Project Overview

This project demonstrates the containerization and deployment of the Wisecow application on Kubernetes using Docker, Minikube, and GitHub Actions CI/CD.

## Features

* Dockerized Wisecow application
* Kubernetes Deployment with multiple replicas
* Kubernetes Service for application exposure
* GitHub Actions CI/CD pipeline
* Automated Docker image build and push to Docker Hub

## Project Structure

```text
.
├── Dockerfile
├── wisecow.sh
├── README.md
├── k8s
│   ├── deployment.yaml
│   └── service.yaml
└── .github
    └── workflows
        └── ci-cd.yml
```

## Docker Build

Build the Docker image:

```bash
docker build -t wisecow:v1 .
```

Run the container:

```bash
docker run -d -p 4499:4499 --name wisecow wisecow:v1
```

## Kubernetes Deployment

Deploy the application:

```bash
kubectl apply -f k8s/
```

Verify deployment:

```bash
kubectl get pods
kubectl get svc
```

## CI/CD Pipeline

GitHub Actions workflow automatically:

1. Checks out source code
2. Authenticates with Docker Hub
3. Builds Docker image
4. Pushes image to Docker Hub

## Verification

Application successfully deployed on Kubernetes and verified through browser access.

### Kubernetes Pods

```bash
kubectl get pods
```

### Kubernetes Services

```bash
kubectl get svc
```

## Technologies Used

* Docker
* Kubernetes
* Minikube
* GitHub Actions
* Docker Hub
* Bash

## Author

Priyanshu Chouhan
