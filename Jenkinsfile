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
    }
    stage('create Docker image') {
            steps {
                echo "building docker image "
                sh "sudo docker build -t project-1 ."
            }
}
