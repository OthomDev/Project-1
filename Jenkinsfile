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
      environment {
        registry = "public.ecr.aws/x8y9i5i2/my-project-repo"
        }
        stage('create Docker image') {
            steps {
                sh "docker build -t project-1 ."
            }
       }
        stage('run Docker Image') {
            steps {
                sh "docker run -d -p 5000:5000 project-1 "
            }
       }
    }
}
