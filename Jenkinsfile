pipeline{
    agent any
    stages{
        stage("Grid Up"){
            steps{
                bat "docker-compose up -d hub chrome firefox"
            }
        }
        stage("Run Tests"){
            steps{
                bat "docker-compose up book-flight-module search-module"
            }
        }

        stage("Grid Down"){
            steps{
                bat "docker-compose down"
            }
        }
    }
}