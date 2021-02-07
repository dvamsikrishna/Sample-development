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
                mvnbuild "mavenbuild"
            }
            post {
                success {
                    echo 'Now Archiving'
                }
            }
        }
    }
}
