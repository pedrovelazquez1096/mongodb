pipeline{
    agent any
    stages{
            stage("Removing supermarketlist-mongodb"){
            steps{
                sh 'docker stop supermarketlist-mongodb'
                sh 'docker rm supermarketlist-mongodb'
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
