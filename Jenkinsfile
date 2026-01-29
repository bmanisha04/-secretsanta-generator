pipeline {
    agent any 
    stages {
        stage ('Checkout') {
            steps {
                checkout scm
            }
        }

        stage ('Build the code') 
        
           steps {
             sh 'mvn clean package'
           }

        stage ('Build') {

            steps{
                sh 'sudo docker build -t secretsanta:latest .'
            }
        }
    }

}