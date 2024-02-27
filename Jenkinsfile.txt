pipeline {
    agent any
    tools {
        nodejs 'nodejs'
    }
    stages {
        stage('Build') {
            steps {                
                bat 'npm install'
            }
        }
        stage('Deploy') {
            steps {
                bat 'npm start'
            }
        }
    }
}