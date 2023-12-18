
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
