pipeline {
    agent {
        label 'jenkinsslave'
    }
    parameters {
        string(name: 'APPLICATION_NAME', description: 'my application', defaultvalue: 'i27app')
        booleanparam(name: 'RUN_TEST', description: 'to run my application', defaultvalue: true)
        choice(name: 'ENV', description: 'to deploy to which environment ?', choices: ['dev','test','prod'])
        password(name: 'PASSWORD', description: 'to enter passsword', defaultvalue: 'SECRET')
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
