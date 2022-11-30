pipeline {
    agent any
      environment {
        K8S_CLUSTER_ID = 'jpw1-caas1-prod1'
        K8S_NAMESPACE = "scv-trino"
    }
    stages {
        stage('scm') {
            steps {
                git branch: 'main', url: 'https://github.com/hemchander007/CaasRepo.git'
            }
        }
        
         stage('k8s') {
            steps {
                
                script{
                   // Apply deployment
                   cpd.kubectl('apply -f Myapp.yml')
                   cpd.kubectl('apply -f service.yml')
                    
                   
               }
                
            }
        }
        
        
    }
}
