pipeline {
    agent any
      environment {
        K8S_CLUSTER_ID = 'jpw1-caas1-prod1'
        K8S_NAMESPACE = "${env.JOB_NAME.split('/')[3]}"
    }
    stages {
        stage('scm') {
            steps {
                git branch: 'main', url: 'https://github.com/ArnabMajumder009/CaasRepo.git'
            }
        }
        
         stage('k8s') {
            steps {
                
                script{
                   // Apply deployment
                   cpd.kubectl('replace --force -f Myapp.yml')
                   cpd.kubectl('replace --force -f service.yml')
                    
                   
               }
                
            }
        }
        
        
    }
}
