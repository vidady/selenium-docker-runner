pipeline{
    agent any
    stages{

        stage("Clean Unused Images"){
            steps{
                bat "docker system prune -f"
            }
        }

        stage("Latest Code Pull"){
            steps{
                bat "docker pull vidady/selenium-docker"
            }
        }


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



    }

    post{
        always{
            archiveArtifacts artifacts:"output/**"
            bat "docker-compose down"
        }
    }
}