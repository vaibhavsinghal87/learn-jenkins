pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo $WORKSPACE
                dir('nodejs-demo') {
                    sh "npm i"
                }
            }
        }
    }
}