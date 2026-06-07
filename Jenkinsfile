pipeline {

    agent any

    stages {

        stage('Clone Code') {
            steps {
                git 'https://github.com/username/docker-jenkins-demo.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t myapp:v1 .'
            }
        }

        stage('Verify Image') {
            steps {
                sh 'docker images'
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