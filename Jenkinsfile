pipeline {
    agent { dockerfile true }
    stages {
        stage ('Checkout') {
          steps {
            git 'https://github.com/rashidhatami/node-bulletin-board.git'
          }
        }
        stage('Build') {
            steps {
                sh 'cd /usr/src/app'
                sh 'docker build -t bulletinboard:1.0 .'
                sh 'docker run --publish 8000:8080 --detach --name bb bulletinboard:1.0'
               
            }
        }
        
    }
}
