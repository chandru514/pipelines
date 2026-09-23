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
                // Installs pytest using pip
                sh 'pip install pytest'
            }
        }
        
        stage('Run Unit Tests') {
            steps {
                // Runs pytest with the verbose (-v) flag
                sh 'pytest -v test_app.py'
            }
        }
    }
}
