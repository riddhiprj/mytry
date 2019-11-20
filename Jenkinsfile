pipeline {
    agent any


    stages {
        stage('gitpull') {
            steps {
                git poll: true, url: 'https://github.com/riddhiprj/mytry.git'
            }
        }
        stage('Build') {
            steps {
                 sh 'mvn -f my/pom.xml package'

            }
        }
        stage('nexus') {
            steps {
            nexusArtifactUploader artifacts: [[artifactId: 'my', classifier: '', file: 'Jenkinsfile', type: 'war']], credentialsId: '9fb5ab08-1b12-4369-837e-994020222232', groupId: 'my', nexusUrl: '192.168.119.134:8081/nexus', nexusVersion: 'nexus2', protocol: 'http', repository: 'snapshots', version: '1.0-SNAPSHOT'
            }      
                
        }
        
        
    }
}
