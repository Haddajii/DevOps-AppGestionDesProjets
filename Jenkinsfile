pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git 'https://github.com/Alaa-Rami/DevOps-AppGestionDesProjets.git'
            }
        }

        stage('Build Docker Images') {
            steps {
                sh 'docker compose build'
            }
        }

        stage('Deploy Application') {
            steps {
                sh 'docker compose up -d'
            }
        }

        stage('Verify Deployment') {
            steps {
                sh 'docker compose ps'
            }
        }
    }
}
