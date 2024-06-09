pipeline{
    agent {
        label 'AGENT-1'
    }
    options{
        timeout(time: 30, unit: 'MINUTES')
        disableConcurrentBuilds()
    }
    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }
    environment{
        Deploy_to = "Production"
        Greetings = "Good Morning"
    }
    stages{
        stage("Build"){
            steps{
                sh 'echo this is build'
            }
        }
        stage("test"){
            steps{
                sh 'echo this is test'
            }
        }
        stage("Deploy"){
            steps{
                sh 'echo this is deploy'
            }
        }
        stage('Params') {
            steps {
                echo "Hello ${params.PERSON}"
                echo "Biography: ${params.BIOGRAPHY}"
                echo "Toggle: ${params.TOGGLE}"
                echo "Choice: ${params.CHOICE}"
                echo "Password: ${params.PASSWORD}"
                echo "triggers"
            }
        }
    }
}