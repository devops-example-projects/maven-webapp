pipeline {
  agent any 
  stages 
  {
    stage('Clean')
    {
      steps {
       sh "/opt/apache-maven-3.6.3/bin/mvn clean"
       }
    }
    stage('Compile')
    {
      steps {
        sh "/opt/apache-maven-3.6.3/bin/mvn compile"
        }
     }
     stage('Test')
     {
       steps {
        sh "/opt/apache-maven-3.6.3/bin/mvn test"
        }
     }
     stage('Package')
     {
      steps {
       sh "/opt/apache-maven-3.6.3/bin/mvn package"
       }
     }
     stage("Archiving")
     {
      steps{
       archiveArtifacts '**/target/*.war'
       }
      }
   }
 }
    
      
      
     
