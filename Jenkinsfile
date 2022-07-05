pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Run pip install
                sh "pip3 install -r requirements.txt"
                
                // Run pytest
                sh "python pytest app-test.py"
            }
        }
    }
}
