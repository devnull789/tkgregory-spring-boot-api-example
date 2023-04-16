pipeline {
    agent any

    triggers {
        pollSCM '* * * * *'
    }
    stages {
        stage('Build') {
            steps {
               sh './gradlew --version'
               sh './gradlew assemble'
            }
        }
        stage('Test') {
            steps {
                sh './gradlew test'
            }
        }
    }
}
