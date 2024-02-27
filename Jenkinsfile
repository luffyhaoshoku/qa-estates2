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
                    bat 'npm run '
                }
                "JsonServer": {
                    bat 'npx json-server db.json --port 8000'
                }      
            )          
            }
        }
    }
}