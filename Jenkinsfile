pipeline {
    agent any
    environment {
        DOCKER_IMAGE = "sheetalkadolkar/express-app:latest"
    }
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/SheetalKadolkar/git-docker-jenkin-project.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                script {
                    docker.build(DOCKER_IMAGE, './backend')
                }
            }
        }
        stage('Push Docker Image') {
            steps {
                script {
                    docker.withRegistry('https://index.docker.io/v1/', 'dockerhub-credentials') {
                        docker.image(DOCKER_IMAGE).push()
                    }
                }
            }
        }
        stage('Run Docker Compose') {
            steps {
                sh 'docker-compose up -d --build'
            }
        }
    }
}
