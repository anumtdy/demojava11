pipeline {
    agent any
    tools{
        maven 'maven'
        }
    stages {
        stage('Build') {
            steps {
                bat 'mvn clean install'
            }
        }
      stage('Deployment') {
            steps {
                pushToCloudFoundry cloudSpace: 'dev', credentialsId: '4ce54de5-315c-4038-8824-6f9f8849efc0', organization: '3cd7cd57trial', target: 'https://api.cf.ap21.hana.ondemand.com'
            }
        }
    }
}
