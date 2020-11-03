pipeline {
  agent any 
  stages 
  {
    stage('Clean')
    {
      steps {
       sh "sudo mvn clean"
       }
    }
    stage('Compile')
    {
      steps {
        sh "sudo mvn compile"
        }
     }
     stage('Test')
     {
       steps {
        sh "sudo mvn test"
        }
     }
     stage('Package')
     {
      steps {
       sh "sudo mvn package"
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
    
      
      
     
