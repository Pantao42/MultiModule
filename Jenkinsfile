pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        git(url: 'git@github.com:Pantao42/MultiModule.git', branch: 'main', changelog: true, poll: true, credentialsId: 'Pantao42')
      }
    }

    stage('Build') {
      steps {
        sh 'mvn clean compile'
      }
    }

  }
}