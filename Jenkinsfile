@Library('jenkins-shared-library@master') _

pipeline {
    agent any
    stages {
        stage('Demo') {
            steps {
                echo 'Calling Shared lib function'
                mvnbuild 'mvnbuild'

            }
        }
    }
}