pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t myapp:v1 .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 8081:80 myapp:v1 || true'
            }
        }
    }
}
