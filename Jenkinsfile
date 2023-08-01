pipeline{
    agent any
    stages{
        stage("Grid Up"){
            steps{
                sh "docker-compose up -d hub chrome firefox"
            }
        }
        stage("Run Tests"){
            steps{
                sh "docker-compose up book-flight-module search-module"
            }
        }

        stage("Grid Down"){
            steps{
                sh "docker-compose down"
            }
        }
    }
}