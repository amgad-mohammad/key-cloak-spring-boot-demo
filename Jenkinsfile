pipeline {
    agent any
    stages {
        stage('Build') {
            agent {
                docker {
                    image 'maven:3.8-eclipse-temurin-11-alpine'
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