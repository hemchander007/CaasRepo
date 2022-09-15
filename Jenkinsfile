pipeline {
    agent any

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
                   cpd.kubectl('apply -f app.yaml')
                   cpd.kubectl('apply -f service.yaml')
                   
               }
                
            }
        }
        
        
    }
}
