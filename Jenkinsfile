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
                sh 'docker rm -f  newwebcontainer'
            }
        }
        stage('Run container'){
            steps {
                sh 'docker run -itd --name container2 -p "5050:80" httpd'
            }
        }
    }
}
