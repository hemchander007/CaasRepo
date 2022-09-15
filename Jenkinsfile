node{
     
    stage('SCM Checkout'){
       git branch: 'main', url: 'https://github.com/ArnabMajumder009/CaasRepo.git'
    }
    
    
    stage('Deploy into K8s'){
    
    sh "cpd.kubectl('apply -f app.yml')"
    
    sh "cpd.kubectl('apply -f service.yml')"
    
    
    }
    
 }
