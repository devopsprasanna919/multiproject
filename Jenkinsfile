pipeline {
    agent {
        label 'jenkinsslave'
    }
    parameters {
        string(name: 'APPLICATION_NAME', description: 'my application', defaultValue: 'i27app')
        booleanParam(name: 'RUN_TESTS', description: 'would you like to run tests ?', defaultValue: true)
        choice(name: 'ENV', description: 'to which environment deploying ?', choices: ['dev','test','prod'])
        password(name: 'PASSWORD', description: 'to enter passsword', defaultValue: 'SECRET')
    }
    stages {
        stage ('buildparameters') {
            steps {
                echo "my application name: ${params.APPLICATION_NAME}"
                echo "are you running test: ${params.RUN_TEST}"
                echo "which environment deploying: ${params.ENV}"
                echo "entered password is: ${params.PASSWORD}"
            }
        }
    }
}
