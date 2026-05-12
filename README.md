# 🚀 CI/CD Pipeline with Jenkins, Docker & AWS EC2

## 📌 Project Overview

Designed and implemented an end-to-end CI/CD pipeline using GitHub, Jenkins, Docker, and AWS EC2 to automate application deployment.

The project automatically builds, containerizes, and deploys a Flask-based web application whenever new code is pushed to the GitHub repository, enabling a fully automated deployment workflow with zero manual intervention.

The deployed application is a restaurant website ("The Biryani Palace") running inside a Docker container on AWS EC2.

---

## 🏗️ CI/CD Workflow

```text
Developer
   ↓
Git Push to GitHub
   ↓
GitHub Webhook Trigger
   ↓
Jenkins Pipeline Execution
   ↓
Docker Image Build
   ↓
Stop & Remove Old Container
   ↓
Deploy Updated Container
   ↓
Live Application on AWS EC2
```

This workflow ensures continuous integration and automated deployment on every push to the main branch.

---

## 🧰 Technologies Used

- Git
- GitHub
- Jenkins
- Docker
- AWS EC2
- Flask (Python)

---

## 📁 Project Structure

```text
CI-CD-project/

├── app.py
├── requirements.txt
├── Dockerfile
├── Jenkinsfile
└── templates/
    └── index.html
```

---

## ⚙️ Jenkins Pipeline Stages

The CI/CD pipeline was implemented using Jenkins Declarative Pipeline and includes the following stages:

- Checkout latest source code from GitHub
- Build Docker image for the Flask application
- Stop and remove the existing running container
- Deploy updated Docker container on AWS EC2
- Log deployment status and pipeline results

GitHub webhooks were configured to automatically trigger the Jenkins pipeline on every code push.

---

## 🌐 Deployment Details

- Application hosted on AWS EC2
- Flask application exposed on port 5000
- Automated container replacement during every deployment
- Continuous deployment enabled through GitHub webhook integration

Each commit pushed to the main branch automatically:

- Triggers the Jenkins pipeline
- Builds a new Docker image
- Replaces the existing running container
- Deploys the updated application to production

---

## 🎯 Key Learnings

- Configured Jenkins on AWS EC2 from scratch
- Implemented webhook-based automated CI/CD workflow
- Managed Docker permissions for Jenkins user
- Debugged pipeline failures and Git authentication issues
- Handled EC2 disk space and swap memory limitations
- Built a repeatable and reliable deployment process
