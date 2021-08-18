pipeline {
    agent {docker}
    stages {
        stage('build') {
            steps {
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
