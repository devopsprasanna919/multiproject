
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
                environmentname: 'TODAY_DAY', value: 'MONDAY'
            }
            steps {
                echo " pipeline for when condition"
            }

        }
    }
}
