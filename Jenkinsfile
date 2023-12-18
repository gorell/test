
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
                    sh 'pip install -r requirements.txt' 
                }
            }
        }

        stage('Run Tests') {
            steps {
                script {
                    sh 'pytest test_add.py'
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
