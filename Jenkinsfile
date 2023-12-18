
pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                script {
                    checkout scm
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    sh 'python -m pytest test_add.py'
                }
            }
        }
    }
}
