pipeline {
    agent any
    stages {
        stage('Echo Version') {
            steps {
                
                sh 'echo Print Maven Version'
                // Command to print Maven version
                sh 'mvn -version'
            }
        }
        stage('Build') {
            steps {
                // Build command with skipTests
                sh 'mvn clean package -DskipTests=true'
            }
        }
        stage('Unit Test') {
            steps {
                // Run unit tests
                sh 'mvn test'
            }
        }
    }
}
