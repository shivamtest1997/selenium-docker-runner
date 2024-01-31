pipeline
{

    agent any

    stages{

        stage("star Grid"){
            steps{
                bat 'docker-compose -f grid.yaml up -d'
            }

        }
        stage("Run Test"){
             steps{
                  bat 'docker-compose up'
            }

        }
    }
    post{
           always{
                    bat 'docker-compose -f grid.yaml down'
                    bat 'docker-compose down'
           }
    }
}
