pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                // Task 15.1: Git commit → Jenkins build
                git 'https://github.com/karand2023b-arch/jenkins-demo.git'
            }
        }
        stage('Compile') {
            steps {
                // Task 15.2: Compile code
                bat 'javac Hello.java' 
            }
        }
        stage('Archive') {
            steps {
                // Task 15.3: Archive artifacts
                // This makes the compiled file available for download
                archiveArtifacts artifacts: '*.class', fingerprint: true 
            }
        }
    }
    post {
        failure {
            // Task 15.4: Fail build on error
            echo 'CI Flow Failed. Please check the compilation logs.'
        }
        always {
            echo 'CI Pipeline execution finished.'
        }
    }
}

