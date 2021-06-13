pipeline {
    agent any
    stages {
        stage('Compiling Stage'){
            steps{
                bat 'python main.py'
            }
        }
        stage('Build Docker'){
            steps{
                bat 'docker build -t main.py .'
            }
        }
        stage('Docker run'){
            steps{
                script{
                    bat 'docker run -ti -p 5000:5000 --name main.py'
                }
            }
        }
    }
