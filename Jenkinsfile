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
                sh 'mvn clean install'
            }
        }
    }
}