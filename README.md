# 🚀 CI/CD Pipeline using Maven, Jenkins, Docker & Kubernetes (EKS)

This project demonstrates a complete **DevOps CI/CD pipeline** to build, containerize, and deploy a Java application on **Amazon EKS (Kubernetes)** using modern tools.

---

## 📌 Project Overview

The goal of this project is to automate the entire software delivery process:

* Build Java application using Maven
* Automate pipeline using Jenkins
* Containerize application using Docker
* Deploy application to Kubernetes (Amazon EKS)

---

## 🏗️ Architecture

```
Developer → GitHub → Jenkins → Docker → Amazon EKS
```

---

## 🛠️ Technologies Used

* Java (Maven)
* Jenkins (CI/CD)
* Docker (Containerization)
* Kubernetes (Amazon EKS)
* AWS (EC2, ECR, EKS)
* Git & GitHub

---

## ⚙️ CI/CD Workflow

1. Developer pushes code to GitHub
2. Jenkins pulls the code
3. Maven builds the application (JAR/WAR)
4. Docker builds image from Dockerfile
5. Image is pushed to AWS ECR
6. Kubernetes (EKS) deploys the application

---

## 📂 Project Structure

```
project-root/
│── src/
│── pom.xml
│── Dockerfile
│── Jenkinsfile
│── k8s/
│    ├── deployment.yaml
│    └── service.yaml
```

---

## 🚀 Setup Instructions

### 1️⃣ Prerequisites

* AWS Account
* Jenkins installed (EC2 recommended)
* Docker installed
* kubectl configured
* EKS cluster setup
* AWS CLI configured

---

### 2️⃣ Build Application

```bash
mvn clean install
```

---

### 3️⃣ Build Docker Image

```bash
docker build -t your-image-name .
```

---

### 4️⃣ Push to AWS ECR

```bash
aws ecr get-login-password --region ap-south-1 | docker login --username AWS --password-stdin <your-account-id>.dkr.ecr.ap-south-1.amazonaws.com

docker tag your-image-name <ecr-repo-url>
docker push <ecr-repo-url>
```

---

### 5️⃣ Deploy to Kubernetes (EKS)

```bash
kubectl apply -f k8s/deployment.yaml
kubectl apply -f k8s/service.yaml
```

---

## 📊 Key Features

* Automated CI/CD pipeline using Jenkins
* Containerized application using Docker
* Kubernetes deployment on AWS EKS
* Scalable and production-ready architecture

---

## 🎯 Learning Outcomes

* Hands-on experience with CI/CD pipelines
* Understanding of Docker and containerization
* Kubernetes deployment and service exposure
* AWS EKS integration

---

## 📌 Future Enhancements

* Add Helm charts for deployment
* Integrate monitoring (Prometheus & Grafana)
* Implement Blue-Green deployment strategy
* Add Terraform for infrastructure automation

---

## 👨‍💻 Author

**Rama Krishna Vankini**
---
