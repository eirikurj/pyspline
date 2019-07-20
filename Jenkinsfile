pipeline {
    agent {
        docker { image 'node:7-alpine' }
    }
    stages {
        stage('Test') {
            steps {
                sh 'pwd'
                sh 'python --version'
                sh 'pip list'
                sh 'pwd'
            }
        }
    }
}