pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Checkout your source code from your version control system (e.g., Git)
                checkout scm 'https://github.com/tousifshah8827/kkkkk.git'
            }
        }
        
        stage('Build') {
            steps {
                // Compile your code (e.g., for a Java project)
                sh 'mvn clean compile'
            }
        }
        
        stage('Test') {
            steps {
                // Run tests (e.g., using JUnit)
                sh 'mvn test'
            }
        }
        
        stage('Package') {
            steps {
                // Package your application (e.g., create a JAR or WAR file)
                sh 'mvn package'
            }
        }
    }
    
    post {
        success {
            // You can perform actions if the pipeline succeeds
            echo 'Build successful! Deploying...'
            // Add deployment steps here
        }
        failure {
            // You can perform actions if the pipeline fails
            echo 'Build failed! Not deploying.'
        }
    }
}
