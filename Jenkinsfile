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
        stage("initialize") {
            steps {
                script {
                    //pipelineUtils.buildJar()
                    echo "Initializing...."
                    echo "Executing pipeline for $BRANCH_NAME"
                }
            }
        }

        stage("test") {
            steps {
                when {
                    expression {
                        BRANCH_NAME == "master"
                    }
                }
                script {
                    //pipelineUtils.buildDockerImage()
                    echo "Testing the application...."
                }
            }
        }

        stage("build") {
            steps {
                when {
                    expression {
                        BRANCH_NAME == "master"
                    }
                }
                script {
                    echo "Building the application"
                }
            }
        }

        stage("deploy") {
            steps {
                when {
                    expression {
                        BRANCH_NAME == "master"
                    }
                }
                script {
                    //pipelineUtils.deploy()
                    echo "Deploying the application...."
                }
            }
        }               
    }
} 
