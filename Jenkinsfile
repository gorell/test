
pipeline {
    agent {
        docker {
            image 'qnib/pytest'
        }
    stages {
        stage('Install') {
            steps {
                script {
                    sh 'pip install pytest'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                     echo 'Start'
                     sh 'PYTHONPATH=. pytest'
                     echo 'End'
                }

            }
        }
    }
}
