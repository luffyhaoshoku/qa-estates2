pipeline {
    agent any    
    stages {
        stage('BatmanBegins') {
            steps {                
                bat 'npm install'
                
            }
        }
        stage('THE DARK KNIGHT SERVER') {
        steps {
            parallel (
                "preview": {
                    bat 'npm start '
                }
                "JsonServer": {
                    bat 'npx json-server db.json --port 8000'
                }      
            )          
            }
        }
    }
}