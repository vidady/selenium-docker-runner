pipeline{
    agent any
    stages{
        stage("Grid Up"){
            steps{
                bat "docker-compose -f 01-selenium-3-grid.yaml up -d hub chrome firefox"
            }
        }
        stage("Run Tests"){
            steps{
                bat "docker-compose -f 01-selenium-3-grid.yaml up search-module"
            }
        }

        stage("Grid Down"){
            steps{
                bat "docker-compose -f 01-selenium-3-grid.yaml down"
            }
        }
    }
}