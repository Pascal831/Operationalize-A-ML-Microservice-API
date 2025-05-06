# Operationalize-A-ML-Microservice-API
# 🚀 Udacity Cloud DevOps Nanodegree Capstone Project

## 📌 Project Summary

This capstone project demonstrates the end-to-end deployment pipeline of a containerized web application using CI/CD tools and Kubernetes on AWS. The process includes setting up Jenkins for automated builds, running linting on code, building and pushing Docker images to Docker Hub, and deploying the application to an Amazon EKS cluster using a blue/green deployment strategy.

---

## 🛠️ Tools & Technologies

- **AWS**: EKS, VPC, CloudFormation
- **CI/CD**: Jenkins
- **Containerization**: Docker, Docker Hub
- **Kubernetes**: Deployment, Services, Blue/Green strategy
- **Other Tools**: kubectl, HTML linter, shell scripting

---

## ⚙️ Setup Overview

### 1. Jenkins Server Setup
A Jenkins server was provisioned on an Ubuntu 18.04 instance with OpenJDK 8 installed. Jenkins was set up and accessed through port 8080 using the default admin credentials.

### 2. IAM Role
Created an IAM role (`EKSRole`) to allow EKS to create and manage required AWS resources.

### 3. Infrastructure Provisioning
VPC and EKS cluster resources were deployed using AWS CloudFormation templates. Verified the resources:
- EKS cluster
- VPC
- Auto Scaling Group
- Worker Nodes

---

## 🔁 CI/CD Pipeline Steps

### ✅ Linting Stage
- Lint HTML
- Lint Dockerfile

### 🐳 Build & Push Docker Image
- Built Docker image locally using Jenkins pipeline
- Pushed Docker image to Docker Hub

### ☸️ Kubernetes Deployment
- Connected to EKS cluster from local machine
- Applied `blue` and `green` deployment controllers
- Created service to expose the deployment via a load balancer
- Used blue/green deployment to switch between environments

---

## 🔍 Validation

### Kubernetes Commands Used
```bash
kubectl get nodes
kubectl get pods
kubectl get services
kubectl describe services/blue-green-lb
```

- Verified that the load balancer routes to the active deployment (blue or green)
- Confirmed autoscaling and service health

---

## 📁 Project Artifacts

- 📄 [Project Report PDF](./Udacity%20Cloud%20DevOps%20Nanodegree%20Capstone%20Project.pdf)

---

## 📬 Contact

Created by **Pascal Egbenda**  
GitHub: [@Pascal831](https://github.com/Pascal831)  
Feel free to explore, fork, and reach out!

---

## ✅ Outcome

Successfully deployed a scalable and automated containerized application using DevOps practices and cloud-native tools!
