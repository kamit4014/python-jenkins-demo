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

                // Use the full path to python.exe on your machine
                bat '"C:\Users\LENOVO\AppData\Local\Microsoft\WindowsApps\python.exe" hello.py'
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
