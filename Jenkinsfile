pipeline {
  agent any
  stages {
    stage('Checking-out-code') {
      steps {
        git(url: 'https://github.com/SaraBenShabbat/docker-demo.git', branch: 'master', credentialsId: 'Git-Creds', poll: true)
      }
    }

    stage('Building') {
      steps {
        sh 'docker build -t docker-demo:latest .'
      }
    }

  }
}