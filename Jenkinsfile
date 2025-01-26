pipeline {

  agent {
    label 'agent1'
  }

  environment {
    DOCKERHUB_SVC_USR=credentials('dockerhub-svc-account')
  }
  
stages {

stage('Login to DockerHub'){
    steps {
    sh('docker login --username $DOCKERHUB_SVC_USR --password $DOCKERHUB_SVC_PSW')
    sh('rm  -rf /root/.docker')
    }
    }









  
}
}
