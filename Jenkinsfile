pipeline {
    agent any
    triggers {
        pollSCM '* * * * *'
    }
    stages {
        stage('Build') {
            steps {
                echo "Building.."
                sh '''
                npm install
                '''
            }
        }
        stage('Test') {
            steps {
                echo "Testing.."
                sh '''
                npm test
                '''
            }
        }
        stage('Deliver') {
            steps {
                echo 'Deliver....'
            }
        }
    }
}
