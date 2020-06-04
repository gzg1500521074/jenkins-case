pipeline {
    agent {
        docker {
            image 'node:12-alpine'
            args '-p 3000:3000'
        }
    }
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                echo "start npm install"
                sh 'npm install --registry=https://registry.npm.taobao.org'
            }
        }
        stage('Test') {
            steps {
                 echo "start run test case"
                 echo "finish run test case"
            }
        }
        stage('Deliver') {
            steps {
                echo "finish deliver"
            }
        }
    }
}