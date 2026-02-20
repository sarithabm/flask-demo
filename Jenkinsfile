pipeline {
    agent any

    stages {

        stage('Clone Code') {
            steps {
                echo 'Cloning from GitHub...'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t flask-app .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 5001:5000 flask-app'
            }
        }
    }
}