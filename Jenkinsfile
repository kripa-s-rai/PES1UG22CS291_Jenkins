pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                eccho 'Building the project...'  
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }
}
