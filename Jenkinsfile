
pipeline {
    agent {
        label 'jenkinsslave'
    }
    environment {
        TODAY_DAY = 'MONDAY'
    }
    stages {
        stage('buildstage') {
            when {
                environment name: 'TODAY_DAY', value: 'MONDAY'
            }
            steps {
                echo " pipeline for when condition"
            }

        }
    }
}
