pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout your source code from your version control system (e.g., Git)
                git 'https://github.com/tousifshah8827/kkkkk.git'
            }
        }
        
        stage('Build') {
            steps {
                // Execute your build commands here (e.g., for a Java project with Maven)
                sh 'test'
            }
        }
        
        stage('Test') {
            steps {
                // Run tests if applicable
                sh 'test compile package'
            }
        }
        
        stage('Deploy') {
            steps {
                // Deploy your application to a staging or production environment
                // (e.g., deploy to a web server, container, or cloud platform)
                sh 'Tomcat9_Server'
            }
        }
    }
}
