pipeline {
    agent {
        docker { image 'node:20.11.1-alpine3.19' }
    }

    stages {
        stage('Show environment') {
            steps {
               sh "node --version"
            }
        }
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
        stage('Close App') {
            steps {
                echo 'Exiting....'
            }
        }
    }
    triggers {
        pollSCM('') //Empty quotes tells it to build on a push
    }
}
