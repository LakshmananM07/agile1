pipeline {
    agent any

    stages {
        // Stage 1: Checkout the code from your repository
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        // Stage 2: Install dependencies (pytest)
        stage('Install Dependencies') {
            steps {
                // Installs pytest into the build environment
                sh 'pip install --user pytest'
            }
        }

        // Stage 3: Run Unit Tests with the verbose flag
        stage('Run Unit Tests') {
            steps {
                // Runs pytest with the verbose (-v) flag as requested
                sh 'python3 -m pytest -v'
            }
        }
    }
}
