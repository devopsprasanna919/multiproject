
pipeline {
    agent {
        label 'jenkinsslave'
    }
    environment {
        name = "sudha"
        course = "aws"
        SONAR_URL = "sonar.hsbsc.com"
        SONAR_CREDS = credentilals('sonar_creds')
    }
    stages {
        stage (fisrst stage) {
            steps {
                echo "welcome ${name}"
                echo "you are enrolled to ${course}"
                echo "printing my token: ${SONAR_CREDS}"
            }
        }
    }
}
