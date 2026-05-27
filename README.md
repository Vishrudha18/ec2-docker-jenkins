# 🚀 Automated Web Application Deployment on AWS EC2 Using Docker and Jenkins

## 📌 Project Overview

This project demonstrates an end-to-end DevOps CI/CD pipeline for deploying a containerized web application on AWS EC2 using Docker and Jenkins.

The application source code is managed through GitHub. Whenever changes are pushed to the repository, Jenkins automatically pulls the latest code, builds a Docker image, creates a new container, and deploys the updated application on an AWS EC2 instance.

---

## 🎯 Objectives

- Automate application deployment using Jenkins
- Containerize applications using Docker
- Host applications on AWS EC2
- Implement Continuous Integration and Continuous Deployment (CI/CD)
- Integrate GitHub with Jenkins for automated builds

---

## 🏗️ Architecture

 Developer
    │
    ▼
 GitHub Repository
    │
    ▼
 Jenkins Server
    │
    ▼
 Docker Build
    │
    ▼
 Docker Container
    │
    ▼
 AWS EC2 Instance
    │
    ▼
 Live Web Application

---

## 🛠️ Technologies Used

| Technology | Purpose |
|------------|----------|
| AWS EC2 | Cloud Hosting |
| Jenkins | CI/CD Automation |
| Docker | Containerization |
| Git | Version Control |
| GitHub | Source Code Repository |
| Nginx | Web Server |
| HTML5 | Frontend Structure |
| CSS3 | Styling |

---

## 📂 Project Structure

ec2-docker-jenkins-demo/
│
├── index.html
├── style.css
├── Dockerfile
└── README.md

---

## ⚙️ Prerequisites

Before starting, ensure the following are available:

- AWS Account
- EC2 Ubuntu Instance
- Jenkins Installed
- Docker Installed
- Git Installed
- GitHub Repository

---

## 🚀 Deployment Steps

### 1. Launch AWS EC2 Instance

- Create Ubuntu EC2 Instance
- Configure Security Groups
- Allow:
  - SSH (22)
  - HTTP (80)
  - Jenkins (8080)

---

### 2. Install Java

sudo apt update
sudo apt install fontconfig openjdk-21-jre -y
java -version

---

### 3. Install Jenkins

sudo wget -O /etc/apt/keyrings/jenkins-keyring.asc \
https://pkg.jenkins.io/debian-stable/jenkins.io-2026.key

echo "deb [signed-by=/etc/apt/keyrings/jenkins-keyring.asc]" \
https://pkg.jenkins.io/debian-stable binary/ | \
sudo tee /etc/apt/sources.list.d/jenkins.list > /dev/null

sudo apt update
sudo apt install jenkins -y

sudo systemctl enable jenkins
sudo systemctl start jenkins

---

### 4. Install Docker

sudo apt install docker.io -y

sudo systemctl enable docker
sudo systemctl start docker

---

### 5. Allow Jenkins to Use Docker

sudo usermod -aG docker jenkins
sudo systemctl restart jenkins

---

### 6. Clone Repository

git clone <repository-url>

---

### 7. Build Docker Image

docker build -t myapp .

---

### 8. Run Docker Container

docker run -d --name myapp -p 80:80 myapp

---

### 9. Access Application

http://<EC2-PUBLIC-IP>

---

## 🐳 Dockerfile

```dockerfile
FROM nginx:latest

COPY . /usr/share/nginx/html

EXPOSE 80
```

---

## 🔄 CI/CD Workflow

1. Developer pushes code to GitHub.
2. Jenkins detects repository changes.
3. Jenkins pulls latest code.
4. Docker image is built automatically.
5. Existing container is stopped and removed.
6. New container is deployed.
7. Updated application becomes live on AWS EC2.

---

## 📸 Project Screenshots

### AWS EC2 Instance

Add screenshot here

### Jenkins Dashboard

Add screenshot here

### Successful Build

Add screenshot here

### Docker Container Running

Add screenshot here

### Live Application

Add screenshot here

---

## 🌟 Key Features

- Automated Deployment
- Docker Containerization
- AWS Cloud Hosting
- Jenkins CI/CD Pipeline
- GitHub Integration
- Responsive Landing Page
- Easy Scalability

---

## 📚 Learning Outcomes

- AWS EC2 Management
- Jenkins Automation
- Docker Container Management
- CI/CD Pipeline Creation
- GitHub Integration
- Cloud Application Deployment

---

## 👨‍💻 Author

**Vishrudha Nagaraj**

Information Technology Student | DevOps Enthusiast

GitHub: https://github.com/yourusername

LinkedIn: https://linkedin.com/in/yourprofile

---

## ⭐ Support

If you found this project useful, consider giving it a ⭐ on GitHub.