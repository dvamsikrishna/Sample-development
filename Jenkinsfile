@Library('jenkins-shared-library@main') _

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
