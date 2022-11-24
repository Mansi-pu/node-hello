pipeline {
  agent any
  stages {
     stage('Git Checkout') {
       steps {
         git branch: 'main', credentialsId: 'git-credentials', url: 'https://github.com/Mansi-pu/node-hello'
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
