pipeline {
    agent {
        label 'jenkinssslave'
    }
    environment {
        DEPLOY_TO = 'production'
    }
    stages {
        stage('deploytoprod') {
            steps {
                echo "deploying to production"
            }
        }
        stage('deploytostage') {
            steps {
                echo "deploying to stage environment"
            }
        }
        stage(deploytodev) {
            when {
                anyOf {
                    branch 'release'
                    environment name: 'DEPLOY_TO', value: 'production'
                }
            }
            steps {
                echo "deploying to dev"
            }
        }
    }
}
