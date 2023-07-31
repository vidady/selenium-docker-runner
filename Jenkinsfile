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
                bat "docker-compose up search-module"
            }
        }

        stage("Grid Down"){
            steps{
                bat "docker-compose down"
            }
        }
    }
}