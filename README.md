🚀 Git–Docker–Jenkins CI/CD Project
📌 Project Overview

This project demonstrates an end-to-end CI/CD pipeline using Git, Docker, and Jenkins.
The pipeline automatically pulls code from GitHub, builds a Docker image, pushes it to Docker Hub, and deploys the application using Docker Compose.

The goal of this project is to gain hands-on DevOps experience by implementing real-world CI/CD practices.

🛠️ Technologies Used

Git & GitHub – Version control and source code management
Docker – Containerization of the application
Docker Hub – Image registry
Docker Compose – Application deployment
Jenkins – CI/CD automation
Node.js & Express.js – Backend application
VS Code – Development environment

📂 Project Structure
git-docker-jenkins-project/
│
├── backend/
│   ├── server.js
│   ├── package.json
│   └── Dockerfile
│
├── frontend/
│   ├── index.html
│   └── style.css
│
├── docker-compose.yml
├── Jenkinsfile
└── README.md

⚙️ How I Created This Project
1️⃣ Application Development

Built a minimal Express.js server
Served a static frontend (HTML + CSS)
Exposed REST API endpoint for testing

2️⃣ Git Version Control

Initialized Git repository
Pushed source code to GitHub
Integrated GitHub repository with Jenkins

3️⃣ Docker Implementation

Created a Dockerfile for the backend
Built Docker images locally
Ran containers using port mapping
Tagged images properly for Docker Hub

4️⃣ Docker Hub Integration

Logged in to Docker Hub
Pushed Docker images to a public repository
Used Docker Hub images during deployment

5️⃣ Jenkins CI/CD Pipeline

Created a Declarative Jenkinsfile
Configured Jenkins credentials securely
Automated the following stages:
Source code checkout from GitHub
Docker image build
Docker image push to Docker Hub
Application deployment using Docker Compose

6️⃣ Deployment with Docker Compose

Used Docker Compose to deploy the application
Enabled easy start/stop of containers
Ensured consistent deployment across environments

▶️ How to Run the Project
🔹 Run Locally (Docker)
docker build -t sheetalkadolkar/express-app:latest ./backend
docker run -d -p 3000:3000 sheetalkadolkar/express-app:latest

🔹 Run Using Docker Compose
docker compose up -d --build


Access the application:

http://localhost:3000

🔄 Jenkins Pipeline Flow
GitHub → Jenkins → Docker Build → Docker Hub → Docker Compose Deployment

Each commit triggers the Jenkins pipeline, ensuring automated build and deployment.

🎯 What I Learned

Practical Git workflow for CI/CD projects
Writing and optimizing Dockerfiles
Docker image tagging and pushing to Docker Hub
Difference between Docker Engine and Docker Compose
Creating Declarative Jenkins Pipelines
Using Jenkins credentials securely
Automating application deployment
Understanding real-world CI/CD pipeline architecture

🧠 Key Takeaway

This project helped me understand how modern DevOps pipelines work in real environments, not just theory.
It strengthened my confidence in working with CI/CD automation, containers, and deployment workflows.
