pipeline {
    agent any

    environment {
        EXTERNAL = 'EXTERNAL'
    }
    
    stages {
        stage('Build') {
            steps {
                echo 'Building...' 
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
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

    post {
        always {
            echo "Pipeline finished."
        }
        success {
            echo "Pipeline succeeded."
        }
    }
}