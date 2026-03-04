pipeline {
    agent any

    stages {

        stage('Clone Repository') {
            steps {
                git 'https://github.com/vinayak872/docker-webapp.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t docker-webapp .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 3001:3000 docker-webapp'
            }
        }

    }
}