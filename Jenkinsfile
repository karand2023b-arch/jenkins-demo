pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building application'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing application'
            }
        }
    }

    post {
        success {
            echo 'Build SUCCESSFUL'
        }
        failure {
            echo 'Build FAILED'
        }
        always {
            echo 'Build finished'
        }
    }
}

