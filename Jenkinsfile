pipeline {
  agent any
  stages {
    stage('Clean Workspace') {
      steps {
        // Clean before build
        cleanWs disableDeferredWipeout: true, deleteDirs: true
        }
    }
    stage('Cloning Git') {
      steps {
        git 'https://github.com/Mansi-pu/node-hello.git'
      }
    } 
    stage('Install Tool') {
      steps {
        sh 'sudo apt install nodejs'
        sh 'node -v'
      }
    }
    stage('Run Application') {
      steps {
        echo 'cd node-hello'
        sh 'npm i'
        sh 'ls'
        sh 'npm start'
      }
    }     
    
  }
}
