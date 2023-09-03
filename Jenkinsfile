pipeline {
    agent {
      label ''
      }
    tools{
        maven 'M2_HOME'
    }
stages{
    stage('Checkout from Github') {
      steps{
         git 'https://github.com/tousifshah8827/kkkkk.git'
           }
       }
      stage('Compile with Maven') {
       steps{
           sh 'mvn clean compile'
              }
            }
       stage('Test with Maven') {
       steps{
           sh 'mvn clean test'
              }
            }
       stage('Package with Maven') {
       steps{
           sh 'mvn clean package'
              }
            }
       stage('Deploy to Prod Server') {
       steps{
           script{
           sshPublisher(publishers: [sshPublisherDesc(configName: 'Tomcat_Server')]
           }
         }
      }
   }
}
