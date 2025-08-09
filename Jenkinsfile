pipeline {
    agent any

    stages {
        stage('w/o dokcer') {
            steps {
                sh 'echo "Without docker"'
            }
        } 

        stage('w/ docker') {
            agent {
                docker {
                    image 'node:18-alpine'
                }
            }

            steps {
                sh '''
                    echo "With docker"
                    npm --version
                '''
            }
        }     
    }
}