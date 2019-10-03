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
            bat 'npm run test'
      }
    }
    stage('Build') {
          steps {
            bat 'npm run build'
      }
    }
  }
}
