pipeline {
    agent any

    stages {
        stage('Validate') {
            steps {
                sh 'node --version'
                sh 'npm --version'
                sh 'spectral --version'
            }
        }
        stage('Deploy') {
            when {
                branch 'master'
            }
            steps {
                echo 'Deploying...'
            }
        }
    }
}