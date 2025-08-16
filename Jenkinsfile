pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out code from GitHub...'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building Python project...'
            }
        }

        stage('Install Dependencies') {
            steps {
                echo 'Installing Python dependencies...'
                bat '"C:\\Users\\LENOVO\\AppData\\Local\\Programs\\Python\\Python313\\python.exe" -m pip install --upgrade pip'
                bat '"C:\\Users\\LENOVO\\AppData\\Local\\Programs\\Python\\Python313\\python.exe" -m pip install -r requirements.txt'
            }
        }

        stage('Test') {
            steps {
                echo 'Running Python tests...'
                bat '"C:\\Users\\LENOVO\\AppData\\Local\\Programs\\Python\\Python313\\python.exe" test_hello.py'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying to AWS...'
                // Example: AWS S3 deployment
                bat 'aws s3 cp hello.py s3://your-bucket-name/'
            }
        }
    }

    post {
        success { echo 'Pipeline completed successfully!' }
        failure { echo 'Pipeline failed!' }
    }
}