pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh '''
                 su jenkins apt-get update
                 su jenkins apt-get install \
                 su jenkins apt-transport-https \
                 ca-certificates \
                 curl \
                 gnupg \
                 lsb-release
                '''
                sh 'docker build -t gcr.io/firststepbruh/express-image:v0.1 . '
            }
        }
        
        stage('test') {
            steps {
                echo 'if you see this wish me a happy life'
            }
        }

        stage('deploy') {
            steps {
                sh 'docker push gcr.io/firststepbruh/express-image:v0.1'
            }
        }
    }
}
