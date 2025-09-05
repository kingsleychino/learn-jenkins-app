pipeline {
    agent any

    stages {
        docker {
            image: 'node:18-alpine'
        }
        stage('w/o docker') {
            steps {
                echo 'Without docker'
            }
        }

        stage('w docker') {
            steps {
                echo 'With docker'
                sh 'npm install'
                sh 'node --version'
                sh 'npm --version'
            }
        }
    }
}