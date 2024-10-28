pipeline {
    agent any
    stages {
        stage('Build') { 
            steps {
                export PATH=$PATH:/usr/local/bin

                sh 'npm install' 
            }
        }
    }
}