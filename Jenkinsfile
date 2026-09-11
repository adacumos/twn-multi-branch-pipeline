@Library('jenkins-shared-library')_

pipeline {
    agent any
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
