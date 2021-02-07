pipeline {
    agent any
    tools {
        maven 'maven'
        jdk 'jdk9'
    }
    stages {
        stage('Build') {
            steps {
                echo 'maven clean'
                bat ' mvn -f pom.xml clean install'  
            }
            post {
                success {
                    echo 'Now Archiving'
                }
            }
        }
    }
}
