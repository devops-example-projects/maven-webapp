pipeline {
  agent any 
  stages {
    stage("Clean")
    {
      steps {
       sh "mvn clean"
       }
    }
    stage("Compile")
    {
      steps {
        sh "mvn compile"
        }
     }
     stage("Test")
     {
       steps {
        sh "mvn test""
        }
     }
     stage("Package")
     {
      steps {
       sh "mvn package"
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
    
      
      
     
