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
