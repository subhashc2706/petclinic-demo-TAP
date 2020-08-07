pipeline {
  agent any
  stages{
    stage ('Build') {
    steps{
      echo "Building Project"
      sh label: '', script: './mvnw package'
      }
     }
     stage ('Archive') {
    steps{
      echo "Archive Project"
     archiveArtifacts artifacts: '**/*.jar', followSymlinks: false
      }
     }
     stage ('Build Docker Image') {
    steps{
      echo "Building Docker Image"
      }
     }
     stage ('push Docker Image') {
    steps{
      echo "pushing Docker Image"
      }
     }
     stage ('Deploy to Dev') {
    steps{
      echo "Deploying to Dev Environment"
      }
     }
   }
      
}
