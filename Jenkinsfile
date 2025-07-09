pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                git url: 'https://github.com/arvind-04/JenkinsDemo.git', branch: 'main'
            }
        }

        stage('Serve index.html') {
            steps {
                echo 'Starting simple HTTP server to serve index.html'
                sh '''
                    python3 -m http.server 8000 &
                    sleep 5
                '''
                echo 'Visit: http://localhost:8000/index.html'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed.'
        }
    }
}
