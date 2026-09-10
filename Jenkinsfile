//def pipelineUtils 

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
                when {
                    expression {
                        BRANCH_NAME == "main"
                    }
                }
                script {
                    //pipelineUtils.buildJar()
                    echo "Building the application...."
                }
            }
        }

        stage("test") {
            steps {
                when {
                    expression {
                        BRANCH_NAME == "main"
                    }
                }
                script {
                    //pipelineUtils.buildDockerImage()
                    echo "Testing the application...."
                }
            }
        }

        stage("deploy") {
            steps {
                when {
                    expression {
                        BRANCH_NAME == "main"
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
