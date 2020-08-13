pipeline {
    agent any

    stages {
        stage('Validate') {
            steps {
                nodejs(nodeJSInstallationName: 'Node.js 12.18.3 (LTS)') {
                    sh 'node --version'
                    sh 'npm --version'
                    sh 'npm config ls'
                    sh 'spectral --version'
                }
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