pipeline {
    
    agent any
    
    stages {
        
        stage('code') {
            
            steps {
                
                git url: ' https://github.com/utkarsh562/portfolio-website.git' , branch: 'master'
            }
        }
        
        stage(' code build ') {
            steps {
                sh 'docker build . -t utkarsh-demo'
            }
        }
        
        stage('Deployment') {
            
            steps {
                sh 'docker-compose down && docker-compose up -d'
            }
        }
    }
}
