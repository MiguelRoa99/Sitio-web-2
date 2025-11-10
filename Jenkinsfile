pipeline {
    agent any

    stages {
        stage('Clonar repositorio') {
            steps {
                git branch: 'main', url: 'https://github.com/MiguelRoa99/Sitio-web-2.git'
            }
        }

        stage('Construir contenedores') {
            steps {
                sh 'docker-compose build'
            }
        }

        stage('Levantar aplicación') {
            steps {
                sh 'docker-compose up -d'
            }
        }

        stage('Verificar servicios') {
            steps {
                sh 'docker ps'
            }
        }
    }
}
