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