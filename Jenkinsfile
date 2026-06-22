pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git 'https://github.com/sivasubramanian0791-hub/springboot-devops-demo.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker build -t springboot-demo .'
            }
        }
    }
}