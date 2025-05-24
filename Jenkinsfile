node{
    stage('Clone Repo') {
              git 'https://github.com/Elavarasi10/Projectwork.git'
            }
        stage('Mvn package') {
             def mvnHome = tool name: 'maven3', type: 'maven'
             def mvnCMD = "${mvnHOME}/bin/mvn"
                sh "${mvnCMD} clean package"
            }
        }
  

