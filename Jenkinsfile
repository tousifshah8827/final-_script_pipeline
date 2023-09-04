pipeline {
    agent any
    
    environment {
        GIT_REPO_URL = 'https://github.com/tousifshah8827/kkkkk.git'
        MAVEN_TOOL = 'M3'
    }
    
    stages {
        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM', 
                          branches: [[name: '*/master']], 
                          userRemoteConfigs: [[url: env.GIT_REPO_URL]]])
            }
        }
    
stage('Build') {
            steps {
                // Build your Java project using Maven
                sh 'mvn clean install'
            }
        }
        
        stage('Test') {
            steps {
                // Run tests, such as JUnit tests
                sh 'mvn test'
            }
        }
        
        stage('Compile') {
            steps {
                // Compile your Java source code (if necessary)
                sh 'mvn compile'
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
            // This block is executed if the pipeline succeeds
            echo 'Build successful!'
        }
        
        failure {
            // This block is executed if the pipeline fails
            echo 'Build failed!'
        }
    }
}
