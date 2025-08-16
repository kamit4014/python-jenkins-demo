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
                // Upgrade pip
                bat '"C:\\Users\\LENOVO\\AppData\\Local\\Programs\\Python\\Python313\\python.exe" -m pip install --upgrade pip'
                // Install requirements if you have a requirements.txt
                bat '"C:\\Users\\LENOVO\\AppData\\Local\\Programs\\Python\\Python313\\python.exe" -m pip install -r requirements.txt'
            }
        }

        stage('Run Python Script') {
            steps {
                echo 'Running hello.py script...'
                bat '"C:\\Users\\LENOVO\\AppData\\Local\\Programs\\Python\\Python313\\python.exe" hello.py'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed. Check console output for details.'
        }
    }
}
