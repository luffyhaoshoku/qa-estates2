pipeline {
    agent any    
    stages {
        stage('BatmanBegins') {
            steps {                
                bat 'npm install'
                bat 'npm start'
            }
        }
        stage('THE DARK KNIGHT SERVER') {
        steps {
            parallel (
                "preview": {
                    bat 'npm run preview'
                }
                "JsonServer": {
                    bat 'npx json-server db.json'
                }      
            )          
            }
        }
    }
}