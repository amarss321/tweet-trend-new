pipeline {
    agent {
        label 'maven'
    }
environment {
    PATH = "/opt/apache-maven-3.9.7/bin:$PATH"
}
    stages {
        stage('Maven-build') {
            steps {
                sh 'mvn clean deploy'
            }
        }
        stage('SonarQube analysis') {
        environment{ 
            scannerHome = tool 'amar-sonar-scanner'
        }
        steps{
        withSonarQubeEnv('amar-sonarqube-server') { // If you have configured more than one global server connection, you can specify its name
        sh "${scannerHome}/bin/sonar-scanner"
                }
            }
        }
    }
}


