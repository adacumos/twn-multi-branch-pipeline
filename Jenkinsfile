@Library('jenkins-shared-library')_

pipeline {
    agent any
    tools {
        maven 'maven-3.9'
    }
    stages {
        stage("build") {
            steps {
                buildJar()
            }
        }

        stage("build docker image") {
            steps {
                buildImage 'adacumos/twn-bootcamp-repo:java-maven-app-1.2'
            }
        }

        stage("deploy") {
            steps {
                deployApp()
            }
        }
    }
}
