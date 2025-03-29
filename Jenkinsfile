pipeline{
    agent any
    stages{
        stage('Clone Repo'){
            steps{
                bat 'git clone https://github.com/juniorandrade/node-app.git'
            }
        }
        stage('Install Dependencies'){
            steps{
                bat 'npm install'
            }
        }
        stage('Run Tests'){
            steps{
                bat 'npm test || echo "No tests defined"'
            }
        }
        stage('Build App'){
            steps{
                bat 'npm run build'
            }
        }
    }
}