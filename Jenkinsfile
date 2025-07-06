pipeline {
    agent any

    tools {
        nodejs "NodeJS 18"
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
