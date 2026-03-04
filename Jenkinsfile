pipeline {
    agent any

    stages {

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t docker-webapp .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 3002:3000 docker-webapp'
            }
        }

    }
}