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
       
  
          stage('Compile and Clean') {
            steps {
                sh "mvn clean compile"
             
            }
        }
        
         stage('Test') {
            steps {
                sh "mvn test"
             
            }
        }
        
         stage('Deploy') {
            steps {
                sh "mvn package"
             
            }
        }
       
     
    

           
        }
    }
