pipeline {
    agent any
    triggers {
        // This block defines triggers for the pipeline
        // In this case, we're using a webhook trigger
        webhook('http://192.168.0.127:8080/github-webhook')
    }
    stages {
        stage('Checkout') {
            steps {
                script {
                    // Checkout code from Git repository
                    checkout scm
                }
            }
        }
        stage('Install Dependencies') {
            steps {
                script {
                    // Install Node.js dependencies
                    sh 'npm install'
                }
            }
        }
        stage('start') {
            steps {
                script {
                    // Run tests
                    sh 'npm start'
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    // Deploy your application
                    sh 'npm start'
                }
            }
        }
    }
}
