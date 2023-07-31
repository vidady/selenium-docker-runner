pipeline{
    agent any
    stages{
        stage("Grid Up"){
            steps{
                bat "docker-compose -f 01-selenium-3-grid.yaml up"
            }
        }
    

        stage("Grid Down"){
            steps{
                bat "docker-compose -f 01-selenium-3-grid.yaml down"
            }
        }
    }
}