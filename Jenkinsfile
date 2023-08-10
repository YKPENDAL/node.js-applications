pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                script {
                    // Checkout code from Git repository
                    checkout scm
                }
            }
        }
        stage('Build') {
            steps {
                script {
                    // Build your Node.js application
                    sh 'npm install'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    // Run tests
                    sh 'npm test'
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
