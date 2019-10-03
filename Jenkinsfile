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
    stage('Deploy') {
        when {
          expression {"$env.GIT_BRANCH" == "origin/master"}
        }
          steps {
            ./node_modules/.bin/firebase deploy --token=$FIREBASE_DEPLOY_TOKEN
          }
        }
  }
}
