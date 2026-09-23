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
                bat 'python -m pip install pytest'
            }
        }
        
        stage('Run Unit Tests') {
            steps {
                // Changed from 'sh' to 'bat' for Windows execution
                bat 'python -m pytest -v test_app.py'
            }
        }
    }
}
