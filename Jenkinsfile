pipeline {
    agent any   
     environment {
            CI = 'true'
        }
    stages {
        stage('Build') {
            steps {
                nodejs('NodeJs'){
                    sh 'npm install'
                }
                
            }
            
        }
        
        stage('Image Build') {
            agent { dockerfile true }
            steps {
                nodejs('NodeJs'){
                    sh 'node version'
                }
            }
        }
        
        stage('Sonarscanner') {
            steps {
                nodejs('NodeJS'){
                    sh 'npm install --save-dev sonarqube-scanner'
                    sh 'node sonarqube-scanner.js'
                } 
            }
                    
                        

    }
}
