pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                sh '''
                export JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto.x86_64
                export PATH=$JAVA_HOME/bin:$PATH

                java -version
                javac -version
                mvn -version

                mvn clean package
                '''
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker build -t springboot-demo .'
            }
        }
    }
}