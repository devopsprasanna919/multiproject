
pipeline {
    agent {
        label 'jenkinsslave'
    }
    environment {
        DEPLOY_TO = 'production'
    }
    stages {
        stage('deploytodev') {
            steps {
                echo "deplyng to dev environment"
            }
        }
        stage('deploytoprod') {
            when {
                allOf {
                    branch 'main'
                    environment name: 'DEPLOY_TO', value: 'production'
                }
            }
            steps {
                echo "pipeline with allOf"
            }
        }
    }
}
