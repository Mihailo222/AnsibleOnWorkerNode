pipeline {

  agent {
    label 'agent1'
  }

  environment {
    DOCKERHUB_SVC=credentials('dockerhub-svc-account')
    VM_SSH_KEYS=credentials('myawesomeprojectwideuser')
  }
  
stages {

stage('Login to DockerHub'){
    steps {
    
    sh('docker login --username $DOCKERHUB_SVC_USR --password $DOCKERHUB_SVC_PSW')
    //echo "***"
    sh("echo $VM_SSH_KEYS")
  
    sh('rm  -rf /root/.docker')

      
    }
}
}


}
