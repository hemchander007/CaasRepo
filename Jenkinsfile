
node{
     
    stage('SCM Checkout'){
        git url: 'https://github.com/ArnabMajumder009/CaasRepo.git',branch: 'main'
    }
    
    
    stage('Deploy into K8s'){
    
    sh './kubectl apply -f app.yml'
    
    sh './kubectl apply -f service.yml'
    
    
    }
    
 }
