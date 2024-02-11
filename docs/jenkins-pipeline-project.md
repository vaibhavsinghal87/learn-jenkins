# Jenkins - Pipeline Project


## Using Pipeline - Script
```
pipeline {
    agent any

    stages {
        stage('Print Workspace') {
            steps {
                echo "${WORKSPACE}"
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
- Only after adding _tools {nodejs 'nodejs-21.6.1'}_, npm i was successful. Why?
