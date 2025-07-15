pipeline {
    agent {
        label 'jenkinsslave'
    }
    parameters {
        string(name: 'APPLICATION_NAME', description: 'my application', defaultValue: 'i27app')
        booleanparam(name: 'RUN_TEST', description: 'would you like to test ?', defaultValue: true)
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
