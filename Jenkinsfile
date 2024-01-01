Jenkinsfile (Declarative Pipeline)

pipeline {
    agent any
    stages {
        stage('Fetch code') {
            steps {
                git branch: 'jenkins-p-build', url: 'https://github.com/Reeceakhun/Dockerizing-Java-Application.git'
            }
        }
    }
}
