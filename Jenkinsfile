pipeline {
    agent any

    stages {
        stage('w/o docker') {
            steps {
                echo 'Without docker'
            }
        }

        stage('w docker') {
            agent {
                docker {
                    image 'node:18-alpine'
                }
            }
            steps {
                echo 'With docker'
                sh 'npm install'
                sh 'node --version'
                sh 'npm --version'
            }
        }
    }
}