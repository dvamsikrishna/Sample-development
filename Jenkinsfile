@Library('jenkins-shared-library@main') _

pipeline {
    agent any
    tools {
        maven 'maven'
        jdk 'jdk9'
    }
    stages {
        stage('Gitclone-mvn branch') {
            steps {
                echo "calling gitclone.groovy function for clone the gir reposiroty"
                gitclone ("https://github.com/dvamsikrishna/Sample-development.git","maven-shared-lib")
               
            }
            
}
        stage('Maven-Build') {
            steps {
                echo "calling the mvnbuild.groovy function for mvn build"
                mvnbuild "mavenbuild"
            }
            
        }
        stage('Gitclone-npm branch') {
            steps {
                echo "calling gitclone.groovy function for clone the gir reposiroty"
                gitclone ("https://github.com/dvamsikrishna/Sample-development.git","npm-shared-lib")
               
            }
            
}
    stage('NPM-Build') {
            steps {
                echo "calling npmbuild.groovy function for npm build"
                npmbuild("gitclone")
            }

}
    stage('Email') {
            steps {
                echo "calling email.groovy shared library function for sending an email"
                 email()
            }
}
}
}
