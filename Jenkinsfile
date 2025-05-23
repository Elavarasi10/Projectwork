pipeline{
    agent any
    stages {
        stage('Clone Repo') {
            steps {
              git 'https://github.com/Elavarasi10/Projectwork.git'
            }
        }
        stage ('Build Docker image'){
            steps {
                sh 'docker pull httpd:latest'
            }
        }
        stage('Remove previous container'){
            steps {
                sh 'docker run -itd --name newwebcontainer -p "5050:80" httpd'
                }
            }
        }
    }
