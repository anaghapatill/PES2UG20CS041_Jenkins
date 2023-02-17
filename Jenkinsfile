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
        sh 'g++ pipeline.cpp'
        sh 'echo "Test Stage Successful"'
        
      }
    }
    stage('Deploy') {
          steps {
            sh '-o pipeline_exec'
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
