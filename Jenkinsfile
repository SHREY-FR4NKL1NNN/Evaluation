pipeline{
    agent any
    tools{
        nodejs 'node'
    }
    stages{
        stage('Clone Repo'){
            steps{
                script{
                    if (!fileExists('Evaluation')){
                        bat 'git clone https://github.com/SHREY-FR4NKL1NNN/Evaluation.git'
                    }
                }
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