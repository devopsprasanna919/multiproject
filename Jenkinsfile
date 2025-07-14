

    pipeline {
    agent {
        label 'jenkinsslave'
    }
    environment {
        DEPLOY_TO = 'production'
    }
    stages {
        stage('deploytodev') {
            when {
                allOf {
                    branch 'main'
                    environment name: 'DEPLOY_TO', value: 'production'
                }
            }
            steps {
                echo "deplyng to dev environment"
            }
        }
        stage('deploytoprod') {
            
            steps {
                echo "pipeline with allOf"
            }
        }
    }
}
