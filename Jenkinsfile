pipeline {
    agent any

    stages {
        stage('Back-end') {
            steps {
                sh 'mvn --version || echo "Maven not installed"'
            }
        }

        stage('Front-end') {
            steps {
                sh 'node --version || echo "Node.js not installed"'
            }
        }

        stage('DB') {
            steps {
                echo "Simulating DB step: MySQL client not available"
            }
        }
    }
}
