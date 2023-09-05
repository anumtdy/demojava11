pipeline {
    agent any
    tools{
        maven 'maven'
        }
    stages {
        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }
      stage('Deployment') {
            steps {
               pushToCloudFoundry cloudSpace: 'dev', credentialsId: '254a456a-8b27-44a3-bee7-5538e31718cc', organization: ' 3cd7cd57trial', target: 'https://api.cf.ap21.hana.ondemand.com'
            }
        }
    }
}
