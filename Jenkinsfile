pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Source code already checked out by Jenkins'
            }
        }

        stage('Compile') {
            steps {
                bat 'javac Hello.java'
            }
        }

        stage('Archive') {
            steps {
                archiveArtifacts '*.class'
            }
        }
    }

    post {
        success {
            echo 'CI Pipeline executed SUCCESSFULLY'
        }
        failure {
            echo 'CI Pipeline FAILED'
        }
    }
}
