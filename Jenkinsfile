pipeline {
    agent any

    stages {
        stage('gitpull') {
            steps {
                sh 'git pull' 'master'
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
