node{
    // Define the GitHub repository URL and your credentials
    def gitRepoUrl = 'https://github.com/tousifshah8827/kkkkk.git'
    //def gitCredentialsId = 'tousifshah8827'
    
    // Define the path where the code will be checked out
    //def checkoutPath = '/path/to/checkout'

    // Define the Maven installation name
    def mavenTool = 'M3'  // The name of the Maven tool configured in Jenkins

    stage('Checkout') {
        // Clone the GitHub repository
        checkout([$class: 'GitSCM', 
                  branches: [[name: '*/master']], 
                  userRemoteConfigs: [[https://github.com/tousifshah8827/kkkkk.git]]])
                  //, credentialsId: tousifshah8827
  }

    stage('Build with Maven') {
        // Set up the Maven tool
        def mvnHome = tool name: mavenTool, type: 'hudson.tasks.Maven$MavenInstallation'

        // Change to the checkout directory
        /*dir(checkoutPath) {
            // Build the project using Maven
            sh "${mvnHome}/bin/mvn clean install"
        }*/
        sh "${mvnHome} clean install"
		//Above mvnHome should be defined in the tools section. 
		//
    }
}
