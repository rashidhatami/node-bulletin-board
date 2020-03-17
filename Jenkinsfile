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
                sh 'docker image build -t bulletinboard:1.0 .'
                sh 'docker container run --publish 8000:8080 --detach --name bb bulletinboard:1.0'
               
            }
        }
        
    }
}
