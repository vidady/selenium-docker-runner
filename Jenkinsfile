pipeline{
    agent any
    stages{
        stage("Grid Up"){
            steps{
                sh "docker-compose -f 01-selenium-3-grid.yaml up -d hub chrome firefox"
            }
        }
        stage("Run Tests"){
            steps{
                sh "docker-compose -f 01-selenium-3-grid.yaml up book-flight-module search-module"
            }
        }

        stage("Grid Down"){
            steps{
                sh "docker-compose -f 01-selenium-3-grid.yaml down"
            }
        }
    }
}