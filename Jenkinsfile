pipeline {
    agent any

    stages {
        stage('gitpull') {
            steps {
                git 'https://github.com/riddhiprj/mytry.git'
            }
        }
        stage('Build') {
            steps {
                 sh 'mvn -f my/pom.xml package'

            }
        }
        stage('Deploy') {
            steps {
                sh 'mvn -f my/target/my.war deploy'
            }
        }
    }
}
