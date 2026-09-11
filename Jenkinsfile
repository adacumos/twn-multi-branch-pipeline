@Library('jenkins-shared-library')_

pipeline {
    agent any
    tools {
        maven 'maven-3.9'
    }
    environment {
        DOCKER_IMAGE = "adacumos/twn-bootcamp-repo:java-maven-app-1.1"
    }
    stages {
        stage("build") {
            steps {
                buildJar()
            }
        }

        stage("build docker image") {
            steps {
                buildImage()
            }
        }

        stage("deploy") {
            steps {
                deployApp()
            }
        }
    }
}
