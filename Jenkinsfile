pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Run pip install
                sh "pip3 install -r requirements.txt"
                
                // Run pytest
                sh "python3 -m pytest app_test.py"
            }
        }
        stage('create Docker image') {
            steps {
                sh "docker build -t project-1 ."
            }
       }
        stage('run Docker Image') {
            steps {
                sh "docker run -d -p 8096:5000 project-1 "
            }
       }
    }
}
