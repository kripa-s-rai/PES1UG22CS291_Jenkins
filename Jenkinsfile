pipeline {
    agent any

    environment {
        REPO_URL = 'https://github.com/kripa-s-rai/PES1UG22CS291_Jenkins.git'
        BRANCH = 'main'
        BINARY_NAME = 'hello'
        SOURCE_FILE = 'hello.cpp'
    }

    stages {
        stage('Clone Repository') {
            steps {
                git branch: BRANCH, url: REPO_URL
            }
        }

        stage('Compile') {
            steps {
                sh 'g++ -o ${BINARY_NAME} ${SOURCE_FILE}'
            }
        }

        stage('Run Executable') {
            steps {
                sh './${BINARY_NAME}'
            }
        }
    }

    post {
        success {
            echo "✅ Build and execution completed successfully!"
        }
        failure {
            echo "❌ Build failed! Check errors."
        }
    }
}
