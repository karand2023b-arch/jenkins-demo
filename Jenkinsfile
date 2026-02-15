pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building the project...'
            }
        }
    }
    post {
        success {
            echo 'SUCCESS: The build finished perfectly!' [cite: 109]
        }
        failure {
            echo 'FAILURE: Something went wrong.' [cite: 109]
        }
    }
}

