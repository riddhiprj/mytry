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
                sh 'mvn package'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
