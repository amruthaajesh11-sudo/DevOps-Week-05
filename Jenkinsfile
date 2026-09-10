pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Checking out source code from GitHub...'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building the application...'
                sh 'python3 app.py'
            }
        }

        stage('Test') {
            steps {
                echo 'Running application tests...'
                sh 'python3 -m pytest test_app.py'
            }
        }
    }
}
