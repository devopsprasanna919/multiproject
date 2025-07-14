
pipeline {
    agent {
        label 'jenkinsslave'
    }
    stages {
        stage('buildstage') {
            when {
                expression { BRANCH_NAME ==~ /(main|release)/ }
            }
            steps {
                echo "expression pipeline"
            }
        }
    }
}
