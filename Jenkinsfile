pipeline {
    agent any 
    stages{
        stage('Start Grid'){
            steps{
                bat "docker-compose up -d hub chrome firefox --no-color"
            }
        }
        stage('Run Test'){
            steps{
                bat "docker-compose up search-module book-flight-module --no-color"
            }
        }
        stage('Stp Grid'){
            steps{
                bat "docker-compose down"
            }
        }
    }
}