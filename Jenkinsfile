pipeline{
    agent any
    stages{
        stage("Stopping supermarketlist-mongodb"){
            steps{
                sh 'docker stop supermarketlist-mongodb'
            }
        }
        stage("Stopping supermarketlist-mongo-express"){
            steps{
                sh 'docker stop supermarketlist-mongo-express'
            }
        }
        stage("Stopping supermarketlist-mysql"){
            steps{
                sh 'docker stop supermarketlist-mysql'
            }
        }
        stage("Stopping supermarketlist-mysqladmin"){
            steps{
                sh 'docker stop supermarketlist-mysqladmin'
            }
        }
        stage("Removing supermarketlist-mongodb"){
            steps{
                sh 'docker rm supermarketlist-mongodb'
            }
        }
        stage("Removing supermarketlist-mongo-express"){
            steps{
                sh 'docker rm supermarketlist-mongo-express'
            }
        }
        stage("Removing supermarketlist-mysql"){
            steps{
                sh 'docker rm supermarketlist-mysql'
            }
        }
        stage("Removing supermarketlist-mysqladmin"){
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