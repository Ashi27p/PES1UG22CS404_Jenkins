pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ missing_file.cpp -o PES1UG22CS404-1'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    sh './PES1UG22CS404-1'
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deployment Successful!'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline Failed!'
        }
    }
}
