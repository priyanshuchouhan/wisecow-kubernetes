# Wisecow Kubernetes Deployment

## Project Overview

This project containerizes and deploys the Wisecow application on Kubernetes using Minikube.

## Components

* Dockerfile
* Kubernetes Deployment
* Kubernetes Service
* GitHub Actions CI/CD

## Deployment Verification

* Docker Image Built Successfully
* Kubernetes Pods Running
* Service Exposed via NodePort
* Application Accessible through Kubernetes

## Commands Used

docker build -t wisecow:v1 .

kubectl apply -f k8s/

kubectl get pods

kubectl get svc
