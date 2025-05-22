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
        stage('Run docker container'){
            steps {
                sh 
                'docker run -itd --name demo-web-container -p "8081:80" httpd'
                    }
            }
        }
}
