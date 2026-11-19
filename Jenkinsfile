pipeline {

    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                dir('backend') {
                    sh './gradlew clean build'
                }
            }
        }

        stage('Test') {
            steps {
                dir('backend') {
                    sh './gradlew test'
                }
            }
        }
    }
}