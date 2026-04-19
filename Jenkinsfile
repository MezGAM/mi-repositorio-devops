pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/MezGAM/mi-repositorio-devops.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t mi-app-flask ./app'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'echo "No hay tests por ahora"'
            }
        }

        stage('Deploy') {
            steps {
                sh 'docker compose down || true'
                sh 'docker compose up -d --build'
            }
        }
    }
}
