pipeline{
    agent any
    stages{
        
        stage("Build/Start container"){
            steps{
                sh 'docker-compose up -d --build'
                sh 'docker ps'
            }
        }
    }
}