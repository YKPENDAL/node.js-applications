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
                    sh 'npm jest'
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
