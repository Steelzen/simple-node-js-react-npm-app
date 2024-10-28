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
        stage('Test') {
            steps {
                sh './jenkins/scripts/test.sh'
            }
        }
        stage('Deliver') {
            steps {
                sh './jenkins/scripts/deliver.sh'
                input message: 'Finished using the web site? (Click "Proceed" to continue)'
                sh './jenkins/scripts/kill.sh'
            }
        }
    }
} 
