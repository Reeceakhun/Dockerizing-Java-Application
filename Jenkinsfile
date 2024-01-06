Jenkinsfile (Declarative Pipeline)

pipeline {
    agent any
    tools {
        maven "MAVEN3"
        jdk "OracleJDK8"
    }
    stages {
        stage ('Build') {
            steps {
                sh 'mvn -s dettings.xml -SskipTests install'
            }
        }

        stage ('test') {
            steps {
                sh 'mvn test'
            }
        }
    }
}
