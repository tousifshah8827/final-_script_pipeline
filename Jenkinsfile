node {
    // Define the GitHub repository URL and your credentials
    def gitRepoUrl = 'https://github.com/tousifshah8827/kkkkk.git'
   
  
    def mavenTool = 'M3'  // The name of the Maven tool configured in Jenkins

    stage('Checkout') {
       
        checkout([$class: 'GitSCM', 
                  branches: [[name: '*/master']], 
                  userRemoteConfigs: [[url: gitRepoUrl]]])
    }

    stage('Build with Maven') {
        // Set up the Maven tool
        def mvnHome = tool name: mavenTool, type: 'hudson.tasks.Maven$MavenInstallation'

        
            sh "${mvnHome}/bin/mvn clean install"
        }*/
        sh "${mvnHome} clean install"
		
    }
}
