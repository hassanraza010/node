pipeline {
    agent any   
     environment {
            CI = 'true'
        }
    stages {
        stage('Build') {
            steps {
                nodejs('NodeJS'){
                    sh 'npm install'
                }
                
            }
            
        }
        
        stage('Image Build') {
            agent { dockerfile true }
            steps {
                nodejs('NodeJS'){
                    sh 'node version'
                }
            }
        }
                    
                        

    }
}
