pipeline {

  agent {
    label 'agent1'
  }

  environment {
    DOCKERHUB_SVC=credentials('dockerhub-svc-account')  //prosledjivanje secreta username, password kroz env
    VM_SSH_KEYS=credentials('ansible_deployed_cloud_vm') //prosledjivanje varijble ssh keys preko env
  }
  
stages {

stage('Login to DockerHub'){
    steps {
    
    sh('docker login --username $DOCKERHUB_SVC_USR --password $DOCKERHUB_SVC_PSW')
    sh("echo \"***\"")
    sh("echo $VM_SSH_KEYS")
    sh("echo $VM_SSH_KEYS_USR")
  
    sh("ssh -i $VM_SSH_KEYS $VM_SSH_KEYS_USR@10.0.1.6")
    
    sh('rm  -rf /root/.docker')

      
    }
}
}


}
