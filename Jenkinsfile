pipeline {
    agent any
    stages {
        stage('Compiling Stage'){
            steps{
                bat 'python src/main.py
            }
        }
        stage('Build Docker'){
            steps{
                bat 'docker build -t src .'
            }
        }
        stage('Docker run'){
            steps{
                     bat 'docker run --rm -i -p 5000:5000 src
            }
        }
    }
}
