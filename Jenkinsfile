pipeline {
  agent any

  stages {
    stage ('Continuous download') {
      steps {
        git branch: 'main', url : 'https://github.com/maniishab/Boardgame.git'
      }
    }

    stage ('Build') {
      steps {
        sh 'mvn clean package -DskipTests'
      }
    }

    stage ('Test') {
      steps {
        sh 'mvn test'
      }
    }

    stage ('Docker build ' ) {
      steps {
        sh 'docker build -t boardgamme:latest . '
      }
    }

  }
}