pipeline {
    agent any 

    stages {
        stage('Checkout') {
            steps {
                // This pulls your code from GitHub/Bitbucket
                checkout scm
            }
        }

        stage('Build Images') {
            steps {
                echo 'Building Docker images...'
                // This triggers your docker-compose file to build the tiers
                sh 'docker-compose build'
            }
        }

        stage('Run Containers') {
            steps {
                echo 'Starting the application...'
                sh 'docker-compose up -d'
            }
        }
    }
}