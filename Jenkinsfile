pipeline {
    agent any
    
    stages {
        stage("git checkout") {
            steps {
                git credentialsId: 'f83c01d6-2eba-41a3-9749-9b0b1b9b5fb7', url: 'https://github.com/sraheeman2/kaseem.git'
            }
        }
        stage("maven build") {
            steps {
                sh 'mvn clean package'
            }
        }
        stage("deploy") {
            steps {
                sshagent(['tomcat-new']) {
                  " " "
            }
        }
    }
}
