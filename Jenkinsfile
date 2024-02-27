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
                a: {
                    bat 'npm run preview'
                }
                b: {
                    bat 'npx json-server db.json'
                }      
            )          
            }
        }
    }
}