@Library('jenkins-shared-library@main') _

pipeline {
    agent any
    tools {
        maven 'maven'
        jdk 'jdk9'
    }
    stages {
        stage('Build') {
            steps {
                npmbuild "npmbuild"
            }
            post {
                success {
                    echo 'Now Archiving'
                }
            }
        }
    }
}
