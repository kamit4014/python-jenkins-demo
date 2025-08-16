pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps {
                echo 'Building Python project...'
            }
        }
        stage('Run') {
            steps {
                // Run your Python script
                bat 'python hello.py'
            }
        }
    }
}
