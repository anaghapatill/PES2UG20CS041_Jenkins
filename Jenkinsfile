pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'echo "Build Stage Successful"'
        
      }
    }
    stage('Test'){
      steps {
        sh 'echo "Test Stage Successful"'
        
        post {
          always {
            junit 'target/surefire-reports/*.xml'
          }
        }
      }
    }
    stage('Deploy') {
          steps {
            sh 'echo "Deployment Successful"'
            
          }
    }
  } 
  post {
    failure {
      echo 'Pipeline failed'
    }
  }
}
