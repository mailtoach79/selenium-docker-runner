pipeline{
    agent any
    stages{
        stage("Start Grid"){
            steps{
                sh "docker-compose up -d hub chrome firefox"
            }
        }
        stage("Run the Test"){
            steps{
                sh "docker-compose up search-module book-flight-module"
            }
        }
        stage("Bring Grid down"){
            steps{
                sh "docker-compose down"
            }
        }
    }
}