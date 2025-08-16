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

                // Use python from PATH
                // On Windows Jenkins, this works if Python is added to System PATH
                bat 'python hello.py' // For Windows agents
                // sh 'python3 hello.py' // Uncomment if using Linux agents
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