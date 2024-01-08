Jenkinsfile (Declarative Pipeline)

pipeline {
    agent any
    tools {
        maven "MAVEN3"
        jdk "OracleJDK8"
    }
    environment {
        SNAP_REPO = 'vprofile-snapshot'
        NEXUS_USER = 'reece'
        NEXUS_PASS = 'reece'
        RELEASE_REPO = 'vprofile-release'
        CENTRAL_REPO = 'vpro-maven-central'
        NEXUSIP = '172.31.27.240'
        NEXUSPORT = '8081'
        NEXUS_GRP_REPO = 'vpro-maven-group'
        NEXUS_LOGIN = 'nexuslogin'
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
