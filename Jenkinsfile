pipeline {
  agent any
  stages {
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
     
    stage('Cloning Git') {
      steps {
        git 'https://github.com/Mansi-pu/node-hello.git'
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
