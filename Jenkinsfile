pipeline{
    agent any
    stages{
        stage("Removing supermarketlist-mongodb"){
            steps{
                sh 'docker stop supermarketlist-mongodb'
            }
            steps{
                sh 'docker rm supermarketlist-mongodb'
            }
        }
        stage("Removing supermarketlist-mongo-express"){
            steps{
                sh 'docker stop supermarketlist-mongo-express'
            }
            steps{
                sh 'docker rm supermarketlist-mongo-express'
            }
        }
        stage("Removing supermarketlist-mysql"){
            steps{
                sh 'docker stop supermarketlist-mysql'
            }
            steps{
                sh 'docker rm supermarketlist-mysql'
            }
        }
        stage("Removing supermarketlist-mysqladmin"){
            steps{
                sh 'docker stop supermarketlist-mysqladmin'
            }
            steps{
                sh 'docker rm supermarketlist-mysqladmin'
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