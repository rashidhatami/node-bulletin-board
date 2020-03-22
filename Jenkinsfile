pipeline {
    //agent { dockerfile true }
    agent any
    stages {
        stage ('Checkout') {
          steps {
            git 'https://github.com/rashidhatami/node-bulletin-board.git'
          }
        }
        stage('Build') {
            steps {
                //sh 'cd /usr/src/app'
                sh 'docker build -t bulletin:1.0 .'
                sh 'docker run --publish 8110:8080 --detach --name bbb bulletin:1.0'
                
               
            }
        }
        
    }
}
