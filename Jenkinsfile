pipeline {
    agent any
    stages {
        stage('Lint') {
            steps {
                script {
                    // Run linter (e.g., ESLint)
                    sh 'npm run lint'
                }
            }
        }
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
                    // Run tests
                    sh 'npm test'
                }
            }
        }
        stage('Package') {
            steps {
                script {
                    // Package the application (e.g., create a tarball or zip file)
                    sh 'npm run build'
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
        stage('Post-Deployment Check') {
            steps {
                script {
                    // Check if the app is running properly
                    sh 'curl http://localhost:3000'
                }
            }
        }
    }
}
