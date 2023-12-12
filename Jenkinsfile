pipeline {
    agent any 
    stages {
        stage('Clean Workspace') {
            steps {
                deleteDir()
            }
        }

        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], userRemoteConfigs: [[url: 'https://github.com/akashrathod7895/webhook-repo1.git']]])
            }
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
