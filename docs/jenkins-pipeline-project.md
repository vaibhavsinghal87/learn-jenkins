# Jenkins - Pipeline Project


## Using Pipeline - Script
```
pipeline {
    agent any
    tools {nodejs 'nodejs-21.6.1'}
    stages {
        stage('Init') {
            steps {
                echo "${WORKSPACE}"
                sh 'npm -v'
            }
        }
        
        stage('Build') {
            steps {
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'jenkins-github-https-creds', url: 'https://github.com/vaibhavsinghal87/learn-jenkins/']])
                dir('nodejs-demo') {
                    sh 'npm i'
                }
            }
        }
    }
}
```

## Using Pipeline - Jenkinsfile
```
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
```

---

## TODO - 
