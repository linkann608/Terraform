pipeline {
    agent none

    stages {
        stage('Back-end') {
            agent {
                docker { image 'maven:3.8.1-adoptopenjdk-11' }
            }
            steps {
                sh 'mvn --version'
            }
        }

        stage('Front-end') {
            agent {
                docker { image 'node:16-alpine' }
            }
            steps {
                sh 'node --version'
            }
        }

        stage('DB') {
            agent {
                docker { image 'mysql' }
            }
            steps {
                // This won't run SQL directly, it's just an example.
                // You need a MySQL client to connect and run real SQL.
                sh 'echo "SELECT * FROM table1;"'
            }
        }
    }
}
