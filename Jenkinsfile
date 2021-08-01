pipeline {
    agent any
    stages {
        stage('git repo & clean') {
            steps {
               sh "rm -rf TicketBookingServiceJunitTesting"
                sh "git clone https://github.com/kishancs2020/TicketBookingServiceJunitTesting.git"
                sh "mvn validate -f TicketBookingServiceJunitTesting"
            }
        }
        stage('validate') {
            steps {
                sh "mvn validate"
            }
        }
        stage('complie') {
            steps {
                sh "mvn compile"
            }
        }
        stage('clean') {
            steps {
                sh "mvn clean"
            }
        }
    }
}
