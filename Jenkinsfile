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
                bat 'docker build -t mi-app-flask ./app'
            }
        }

        stage('Run Tests') {
            steps {
                bat 'echo No hay tests por ahora'
            }
        }

        stage('Deploy') {
            steps {
                bat 'docker compose down || exit 0'
                bat 'docker compose up -d --build'
            }
        }
    }
}
