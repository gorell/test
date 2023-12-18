
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

        stage('Install dependencies') {
            steps {
                script {
                    sh 'pip install' 
                }
            }
        }

        stage('Run Tests') {
            steps {
                script {
                    sh 'python -m pytest test_add.py'
                }
            }
        }
    }

    post {
        always {
            echo "end"
        }
    }
}
