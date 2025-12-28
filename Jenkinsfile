pipeline {
    agent any
    stages {
        stage('Build') {
            agent {
                docker {
                    image 'maven:3.9-eclipse-temurin-21-alpine'
                    reuseNode true
                }
            }
            steps {
                sh 'mvn --version'
                sh 'mvn clean compile'
            }
        }
        stage('Test') {
            agent {
                docker {
                    image 'maven:3.9-eclipse-temurin-21-alpine'
                    reuseNode true
                }
            }
            steps {
                sh 'echo "Starting Tests!"'
                sh 'mvn test'
            }
        }
    }
}