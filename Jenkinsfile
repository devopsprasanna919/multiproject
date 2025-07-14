
pipeline {
    agent {
        label 'jenkinsslave'
    }
    stages {
        stage('buildstage') {
            when {
                expression { BRANCH_NAME ==~ /(main|feature)/ }
            }
            steps {
                echo "expression pipeline"
            }
        }
    }
}
