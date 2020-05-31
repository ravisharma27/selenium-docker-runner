pipeline {
    agent any 
    stages{
        stage('Pull Latest Image'){
            steps{
                bat "docker pull ravisharma2780/selenium-docker1"
            }
        }
        stage('Start Grid'){
            steps{
                bat "docker-compose up -d hub chrome firefox"
            }
        }
        stage('Run Test'){
            steps{
                bat "docker-compose up search-module book-flight-module"
            }
        }
    }
    post{
        always {
            bat "docker-compose down"
        }
    }
}