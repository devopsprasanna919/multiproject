pipeline {
    agent {
        label 'jenkinsslave'
    }
    stages {
        stage('build') {
            steps {
                echo "***deploying to build"
            }
        }
        stage('dockerbuild') {
            steps {
                echo "***deploying to docker build"
            }
        }
        stage('sonarbuild') {
            steps {
                echo "deploying to sonar"
            }
        }
        stage('stage') {
            when {
                branch 'main*'
            }
            echo "deploying to stageenvironment"
        }
        stage('production') {
            when {
                tag pattern: "v\\d{1,2}.d{1,2}.d{1,2}", comparator: "REGEXP"
            }
            steps {
                echo "deploying to production environment"
            }
        }
    }
}
