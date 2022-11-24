pipeline {
  agent any
  stages {
    stage('Clean Workspace') {
      steps {
        // Clean before build
        cleanWs disableDeferredWipeout: true, deleteDirs: true
        }
    }
    stage('Install Tool') {
      steps {
        sh 'sudo apt install nodejs'
        sh 'node -v'
      }
    }
    stage('Install dependencies') {
      steps {
        sh 'npm install'
        sh 'npm -v'
      }
    } 
    stage('Install Express') {
      steps {
        echo 'cd node-hello'
        sh 'npm i express'
      }
    } 
    stage('Run Application') {
      steps {
        echo 'cd node-hello'
        sh 'npm start'
      }
    }     
    
  }
}
