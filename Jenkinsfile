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
    }
}

#amarnath
