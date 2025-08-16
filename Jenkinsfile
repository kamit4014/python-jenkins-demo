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

        stage('Run Python Script') {
            steps {
                echo 'Running hello.py script...'

                // Use correct installed Python path
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