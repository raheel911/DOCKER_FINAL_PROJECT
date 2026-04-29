pipeline {
    agent any 

    stages {
        stage('Build and Run') {
            steps {
                script {
                    // Use the plugin's built-in docker features
                    echo 'Building and starting containers...'
                    sh 'docker compose build' 
                    sh 'docker compose up -d'
                }
            }
        }
    }
}