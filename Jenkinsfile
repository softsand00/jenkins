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
        stage('Test') {
            steps {
                script {
                    // Run tests (add your tests here)
                    sh 'echo "Running tests..."'
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
    }
}
