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
                	sh " ansible-playbook ansible/build.yml -i ansible/inventory/host.yml -e ansible_become_password=ubuntu"
                	
                }
             
         
             
            }
        }
     stage('docker'){
            steps{
                script{
                    sh " ansible-playbook ansible/docker.yml -i ansible/inventory/host.yml -e ansible_become_password=ubuntu"
                }
            }
        }

           
        }
    }
