pipeline {
  agent any
  stages {
    stage('sourcing code') {
      steps {
        sh 'git clone https://github.com/stephanemiafo/Containerized-apache-webserver.git'
      }
    }

    stage('build stage') {
      steps {
        sh 'docker build -t myimage:01 .'
      }
    }

    stage('run stage') {
      steps {
        sh 'docker run -itd --name apache -p 4000:80'
      }
    }

  }
}