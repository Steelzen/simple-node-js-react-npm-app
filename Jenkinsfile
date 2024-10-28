pipeline {
    agent any
    environment {
        PATH = "${env.PATH}:/usr/local/bin" // Sets the PATH globally for the pipeline
    }
    stages {
        stage('Build') { 
            steps {
                sh 'npm install'  // Runs npm install
            }
        }
    }
} 
