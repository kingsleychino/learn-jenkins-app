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
                    reuseNode true
                }
            }
            steps {
                sh '''
                    echo "With docker"
                    ls -la
                    touch container-yes.txt
                '''
            }
        }
    }
}