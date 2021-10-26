pipeline {
    agent { docker { image 'python:latest'}}

    environment {
        PROJECT_NAME = "MY PIPLINE"
    }

    stages {
        stage('My-Build-Stage-1') {
            steps {
                echo "Hello world"
            }
        }
        stage('My-Build-Stage-2') {
            steps {
                echo "step 2"
                sh '''
                ls /var/log
                date
                echo ${PROJECT_NAME}
                '''
            }
        }
        stage('Test-Stage') {
            steps {
                sh "ls -lah /etc"
                sh "python --version"
            }
        }
    }    
}