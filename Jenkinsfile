
pipeline {
    agent {
        docker {
            image 'qnib/pytest'
        }
    }
    stages {
        stage('Test') {
            steps {
                script {
                     sh 'python -m pytest'
                }
            }
        }
    }
}
