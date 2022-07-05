pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Run pip install
                sh "pip install -r requirements.txt"
                
                // Run pytest
                sh "python3 pytest app-test.py"
            }
        }
    }
}
