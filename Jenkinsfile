pipeline{
    agent any
    stages{
        stage("Removing supermarketlist-mongodb"){
            steps{
                sh 'docker stop supermarketlist-mongodb'
                sh 'docker rm supermarketlist-mongodb'
            }
        }
        stage("Removing supermarketlist-mysql"){
            steps{
                sh 'docker stop supermarketlist-mysql'
                sh 'docker rm supermarketlist-mysql'
            }
        }
        stage("Removing sqlserver"){
            steps{
                sh 'docker stop sqlserver'
                sh 'docker rm sqlserver'
            }
        }
        stage("Build/Start container"){
            steps{
                sh 'docker-compose up -d --build'
                sh 'docker ps'
            }
        }
    }
}