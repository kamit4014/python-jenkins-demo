pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps { checkout scm }
        }

        stage('Build') {
            steps { echo 'Building Python project...' }
        }

        stage('Run Python Script') {
            steps {
                echo 'Running hello.py script...'
                bat '"C:/Users/LENOVO/AppData/Local/Microsoft/WindowsApps/python.exe" hello.py'
            }
        }
    }

    post {
        success { echo 'Pipeline completed successfully!' }
        failure { echo 'Pipeline failed. Check console output for details.' }
    }
}
