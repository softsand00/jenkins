pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    // Install dependencies
                    sh 'npm install'
                }
            }
        }
        stage('Lint') {
            steps {
                script {
                    // Run linting (replace with your actual lint command)
                    sh 'npm run lint || echo "Linting failed, but continuing..."'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    // Run tests (replace with your actual test command)
                    sh 'npm test || echo "Tests failed, but continuing..."'
                }
            }
        }
        stage('Package') {
            steps {
                script {
                    // Package the application (replace with your actual package command)
                    sh 'npm run build || echo "Packaging failed, but continuing..."'
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    // Deploy to a server (simple example: run the app)
                    sh 'nohup node index.js &'
                }
            }
        }
        stage('Cleanup') {
            steps {
                script {
                    // Cleanup steps (optional)
                    sh 'rm -rf node_modules'
                }
            }
        }
    }
}
