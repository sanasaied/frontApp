pipeline {
    agent any
    stages {
          stage('Checkout GIT') {
            steps {
                echo 'Pulling...';
                git branch: 'main',
                url : 'https://github.com/sanasaied/frontApp.git'
             
         
             
            }
        }
       
     
      stage('Build') {
            steps {
                script{
                	sh " ansible-playbook ansible/build.yml -i ansible/inventory/host.yml "
                	
                }
             
         
             
            }
        }
    

           
        }
    }
