pipeline {
    agent any

    stages {
        stage('Back-end') {
            steps {
                script {
                    docker.image('maven:3.8.1-adoptopenjdk-11').inside {
                        sh 'mvn --version'
                    }
                }
            }
        }

        stage('Front-end') {
            steps {
                script {
                    docker.image('node:16-alpine').inside {
                        sh 'node --version'
                    }
                }
            }
        }

        stage('DB') {
            steps {
                script {
                    docker.image('mysql').inside {
                        sh 'echo "SELECT * FROM table1;"'
                    }
                }
            }
        }
    }
}
