pipeline{
    agent any

    environment {
        DOCKERHUB_CREDENTIALS=credentials('dockerhub')
    }
    stages {
        stage('Clone Repo') {
            steps {
              git 'https://github.com/Elavarasi10/Projectwork.git'
            }
        }
        stage ('Build Docker image'){
            steps {
                sh 'docker build -t elavarasi10/demo-webapp:latest .'
            }
        }
        stage('login'){
            steps {
                sh 'echo $DOCKERHUB_CREDENTIALS_PSW | docker login -u $DOCKERHUB_CREDENTIALS_USR --pass'
            }
        }
        stage('login'){
            steps {
                sh 'docker push elavarasi10/demo-webapp:latest'
            }
        }
    }
}
