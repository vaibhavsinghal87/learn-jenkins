pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                dir('nodejs-demo') {
                    sh "npm i"
                }
            }
        }
    }
}