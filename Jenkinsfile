// Triggering build via GitHub webhook
// Added dummy line to re-trigger webhook

pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Listing .java files in repo:'
                bat 'dir /s *.java'

                echo 'Compiling Java files:'
                bat 'javac HelloWorld.java'
            }
        }

        stage('Run') {
            steps {
                echo 'Running Java program:'
                bat 'java HelloWorld'
            }
        }
    }
}
