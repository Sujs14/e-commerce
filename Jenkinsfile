pipeline {
    agent any

    tools {
        nodejs "Node-18"
    }

    stages {

        stage('Clone Repository') {
            steps {
                git 'https://github.com/Sujs14/e-commerce.git'
            }
        }

        stage('Install Backend Dependencies') {
            steps {
                dir('backend') {
                    sh 'npm install'
                }
            }
        }

        stage('Install Frontend Dependencies') {
            steps {
                dir('frontend') {
                    sh 'npm install'
                }
            }
        }

        stage('Build Frontend') {
            steps {
                dir('frontend') {
                    sh 'npm run build'
                }
            }
        }

        stage('Test') {
            steps {
                echo 'Add testing command here if available'
            }
        }

        stage('Deploy (Optional)') {
            steps {
                echo 'Deployment stage here'
            }
        }
    }
}

