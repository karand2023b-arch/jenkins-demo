pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                bat 'echo Building the project...' 
            }
        }
    }
    post {
        success {
            echo 'Appropriate message displayed: Build Successful!'
        }
        failure {
            echo 'Appropriate message displayed: Build Failed!'
        }
    }
}
