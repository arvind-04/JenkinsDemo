pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Building the project......'
                sh 'echo Simulating build process...'
                // For real projects: sh 'npm install' or 'mvn clean install' etc.
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'echo Simulating tests...'
                // For real projects: sh 'npm test' or 'mvn test' etc.
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                sh 'echo Simulating deployment...'
            }
        }
    }

    post {
        success {
            echo '✅ Pipeline completed successfully.'
        }
        failure {
            echo '❌ Pipeline failed.'
        }
    }
}
