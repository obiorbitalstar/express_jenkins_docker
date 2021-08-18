pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh 'docker build -t obiorbitalstar/node-web-app .  '
            }
        }
        
        stage('test') {
            steps {
                echo 'if you see this wish me a happy life'
            }
        }

        stage('deploy') {
            steps {
                sh 'docker run -it -p 3000:3000 obiorbitalstar/node-web-app'
            }
        }
    }
}
