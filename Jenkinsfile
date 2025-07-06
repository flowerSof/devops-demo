pipeline {
    agent {
        docker {
            image 'node:18'
            reuseNode true
        }
    }
    stages {
        stage('Clonar') {
            steps {
                git 'https://github.com/flowerSof/devops-demo.git'
            }
        }
        stage('Instalar dependencias') {
            steps {
                sh 'npm install'
            }
        }
        stage('Ejecutar app') {
            steps {
                sh 'node index.js &'
            }
        }
    }
}
