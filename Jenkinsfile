pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm ci'
            }
        }

        stage('Test') {
            steps {
                sh 'node --version'
                sh 'npm --version'
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker build -t devops-task-3 .'
            }
        }
    }
}
