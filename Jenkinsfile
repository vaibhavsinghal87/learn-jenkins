pipeline {
    agent any
    tools {nodejs "latest"}
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