pipeline {
    agent any
    
    environment {
        GIT_REPO_URL = 'https://github.com/tousifshah8827/kkkkk.git'
        MAVEN_TOOL = 'M3'
    }
    stages {
        stage('Checkout') {
            steps {
                echo "###########tousif4##########"
                checkout([$class: 'GitSCM', 
                          branches: [[name: '*/master']], 
                          userRemoteConfigs: [[url: env.GIT_REPO_URL]]])
                echo "############tousif1######"
stages{'Compile with M3'} { 
    echo "###############tousif2#############"
                    steps {
                        echo "##############tousif3###################"
                         sh 'mvn clean compile'
                    }
                }
            }
        }
    }
}
