pipeline {
    agent any
    

    stages {
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
