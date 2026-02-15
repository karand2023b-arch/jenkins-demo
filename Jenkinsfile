pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/your-username/your-repo.git'
            }
        }

        stage('Compile') {
            steps {
                bat 'javac Hello.java'
            }
        }
    }

    post {
        success {
            archiveArtifacts '*.class'
            echo 'Build & Archive SUCCESS'
        }
        failure {
            echo 'Build FAILED'
        }
    }
}

