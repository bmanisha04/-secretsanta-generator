pipeline {
    agent any 
    stages {
        stage ('Checkout') {
            steps {
                checkout scm
            }
        }

        stage ('Build') {

            steps{
                sh 'mvn clean package -DskipTests'
                sh 'sudo docker build -t secretsanta:latest .'
            }
        }
    }

    post{
        always{
            cleanWs()
        }
    }

}