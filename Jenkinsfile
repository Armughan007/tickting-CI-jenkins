pipeline {
    agent any
    stages {
        stage('git repo & clean') {
            steps {
              // bat "rmdir  /s /q TicketBookingServiceJunitTesting"
                bat "git clone https://github.com/Armughan007/tickting-CI-jenkins.git"
               // bat "mvn clean -f tickting-CI-jenkins"
            }
        }
        stage('install') {
            steps {
                bat "mvn install -f tickting-CI-jenkins"
            }
        }
        stage('test') {
            steps {
                bat "mvn test -f tickting-CI-jenkins"
            }
        }
        stage('package') {
            steps {
                bat "mvn package -f tickting-CI-jenkins"
            }
        }
    }
}
