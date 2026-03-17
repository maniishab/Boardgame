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
  }
}