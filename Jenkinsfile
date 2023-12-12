pipeline {
    agent any 
    stages {
        stage ("clonerepo") {
            steps {
                sh "git clone https://github.com/akashrathod7895/webhook-repo1.git"
                
                
            }
            
        }
        stage ("copyindexfile") {
            steps {
                sh "yum install httpd -y"
                sh "service httpd start"
                sh "chkconfig httpd on"
                sh "chmod -R 777 /var"
                sh "cd /var/www/html"
                sh "cp /root/.jenkins/workspace/project/index.html ."
                
                
            }
            
        }
        
    }
    
    
}
