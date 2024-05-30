pipeline {
    agent {
        label 'maven'
    }
    stages {
        stage('Clone-code') {
            steps {
                script {
                    git branch: 'main', url: 'https://github.com/amarss321/tweet-trend-new.git'
                }
            }
        }
    }
}

