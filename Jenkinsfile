
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                script {
                    // Assuming your code is in a Git repository
                    checkout scm
                }
            }
        }

        stage('Install dependencies') {
            steps {
                script {
                    // Install required dependencies
                    sh 'pip install -r requirements.txt'  // If you have any dependencies
                }
            }
        }

        stage('Run Tests') {
            steps {
                script {
                    // Run pytest
                    sh 'pytest test_add.py'
                }
            }
        }
    }

    post {
        always {
            // Clean up or post-process steps can go here
        }
    }
}
