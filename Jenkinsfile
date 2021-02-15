@Library('jenkins-shared-library@main') _

pipeline {
    agent any
    tools {
        maven 'maven'
        jdk 'jdk11'
    }
    stages {
        stage('Build') {
            steps {
                mvnbuild ""
            }
            post {
                success {
                    echo 'Now Archiving'
                }
            }
        }
    }
}
