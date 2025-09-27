pipeline {
    agent any

    stages {
        stage('Verify tooling'){
            steps{
                bat 'docker --version'
                bat 'docker-compose --version'
            }
        }

        stage('checkout'){
            steps{
                checkout scmGit(
                branches: [[name: '*/main']], 
                extensions: [], 
                userRemoteConfigs: [[url: 'https://github.com/IbekweVictor/Simple-flaskApp.git']])
            }
        }

        stage('Activate Docker-compose'){
            steps{
                bat 'Docker-compose up -d'
            }
        }

        stage('Test Application'){
            steps{
                sleep 10
                bat 'curl http://localhost:5000'
            }
        }

        stage('Show running containers'){
            steps{
                bat 'docker ps'
            }
        }
    }

    post {
        always {
            bat 'docker-compose down'
        }
        success {
            echo 'Build Success'
        }
    failure {
        echo 'Build Failed'
        }
    }
}
