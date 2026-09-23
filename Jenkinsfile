pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Install Dependencies') {
            steps {
                // Changed from 'sh' to 'bat' for Windows execution
                bat 'pip install pytest'
            }
        }

        stage('Run Unit Tests') {
            steps {
                // Changed from 'sh' to 'bat' and used the standard Windows python command
                bat 'python -m pytest -v'
            }
        }
    }
}
