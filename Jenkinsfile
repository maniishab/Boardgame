pipeline {
agent any

environment {
ACR_LOGIN_SERVER = "devopsproject2.azurecr.io"
IMAGE_NAME = "boardgame"
TAG = "latest"
}

parameters {
choice(
name: 'ENV',
choices: ['Dev', 'Test', 'Prod'],
description: 'Select Env'
)
}

stages {

```
stage('Continuous Download') {
  steps {
    git branch: 'main', url: 'https://github.com/maniishab/Boardgame.git'
  }
}

stage('Build') {
  steps {
    sh 'mvn clean package -DskipTests'
  }
}

stage('Test') {
  steps {
    sh 'mvn test'
  }
}

stage('Docker Build') {
  steps {
    sh 'docker build -t ${IMAGE_NAME}:${TAG} .'
  }
}

stage('Login to ACR') {
  steps {
    withCredentials([usernamePassword(
      credentialsId: 'acr-creds',
      usernameVariable: 'ACR_USER',
      passwordVariable: 'ACR_PASS'
    )]) {
      sh '''
        echo $ACR_PASS | docker login $ACR_LOGIN_SERVER \
        -u $ACR_USER --password-stdin
      '''
    }
  }
}

stage('Tag Image') {
  steps {
    sh '''
      docker tag ${IMAGE_NAME}:${TAG} \
      $ACR_LOGIN_SERVER/${IMAGE_NAME}:${TAG}
    '''
  }
}

stage('Push Image to ACR') {
  steps {
    sh 'docker push $ACR_LOGIN_SERVER/${IMAGE_NAME}:${TAG}'
  }
}

stage('Deploy to Kubernetes') {
  steps {
    sh 'kubectl apply -f deployment.yml'
  }
}
```

}
}
