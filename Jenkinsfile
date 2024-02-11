pipeline {
    agent any
    tools {nodejs 'nodejs-21.6.1'}
    stages {
        stage('Build') {
            steps {
                echo "${WORKSPACE}"
                dir('nodejs-demo') {
                    sh 'npm i'
                }
            }
        }
    }
}