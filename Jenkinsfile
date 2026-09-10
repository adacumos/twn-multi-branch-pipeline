def pipelineUtils 

pipeline {   
    agent any
    /*tools {
        maven 'maven-3.9'
    }
    environment {
        DOCKER_IMAGE = "adacumos/twn-bootcamp-repo:java-maven-app-1.1"
    }*/
    stages {
        /*stage('initialize') {
            steps {
                script {
                    pipelineUtils = load 'pipelineUtils.groovy'
                }
            }
        }*/
        stage("build") {
            steps {
                script {
                    //pipelineUtils.buildJar()
                    echo "Building the application...."
                }
            }
        }

        stage("test") {
            steps {
                script {
                    //pipelineUtils.buildDockerImage()
                    echo "Testing the application...."
                }
            }
        }

        stage("deploy") {
            steps {
                script {
                    //pipelineUtils.deploy()
                    echo "Deploying the application...."
                }
            }
        }               
    }
} 
