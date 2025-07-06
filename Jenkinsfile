pipeline {
    agent any
    stages {
        stage('Clonar') {
            steps {
                git 'https://github.com/flowerSof/devops-demo.git'
            }
        }
        stage('Instalar') {
            steps {
                sh 'npm install'
            }
        }
        stage('Build Docker') {
            steps {
                sh 'docker build -t devops-demo .'
            }
        }
        stage('Desplegar') {
            steps {
                sh 'docker run -d -p 3000:3000 devops-demo'
            }
        }
    }
}
