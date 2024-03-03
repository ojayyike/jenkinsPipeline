pipeline {
    agent any
    

    stages {
        stage('Build') {
            // steps {
            //     echo 'Building..'
            // }
             // stage('Build') {
            agent {
                docker {
                    image 'gradle:8.2.0-jdk17-alpine'
                    // Run the container on the node specified at the
                    // top-level of the Pipeline, in the same workspace,
                    // rather than on a new node entirely:
                    reuseNode true
                }
            }
            steps {
                sh 'gradle --version'
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
