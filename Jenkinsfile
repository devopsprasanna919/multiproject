
pipeline {
    agent {
        label 'jenkinsslave'
    }
    stages {
        stage ('build') {
            steps {
                echo ('build from main branch')
            }
        stage ('scam') {
            steps {
                echo ('scam from feature branch')
            }
        stage ('deploy') {
            steps {
                echo ('deploy from hotfix branch')
            }
        }
        }
        }
    }
}
