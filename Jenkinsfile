pipeline {
    agent any
    stages {
        stage("build") {
            when {
                expression {
                    BRANCH_NAME == "main"
                }
            }
            steps {
                echo "Building the application...."
            }
        }

        stage("test") {
            when {
                expression {
                    BRANCH_NAME == "main"
                }
            }
            steps {
                echo "Testing the application...."
            }
        }

        stage("deploy") {
            when {
                expression {
                    BRANCH_NAME == "main"
                }
            }
            steps {
                echo "Deploying the application...."
            }
        }
    }
}
