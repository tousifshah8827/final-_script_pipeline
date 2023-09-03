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
                stages{'Compile with Maven'} {
                    step{
                         sh 'clean compile'
                    }
                }
            }
        }
    }
}
