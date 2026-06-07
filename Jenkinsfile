pipeline {
    agent any

    stages {

        stage('Clone Code') {
            steps {
                echo 'Repository Checked Out'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t myapp:v1 .'
            }
        }

        stage('Verify Image') {
            steps {
                bat 'docker images'
            }
        }
    }

    post {
        success {
            echo 'Docker Image Built Successfully'
        }

        failure {
            echo 'Build Failed'
        }
    }
}