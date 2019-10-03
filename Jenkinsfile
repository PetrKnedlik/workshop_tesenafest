pipeline {
  agent any
  environment {
    CI = 'true'
  }
  stages {
    stage('Install') {
      steps {
        bat 'npm install'
      }
    }
    stage('Start') {
      steps {
        bat 'npm start'
       }
    }
    stage('Test') {
          steps {
            bat 'npm test'
          }
    }
  }
}
