pipeline{
    agent {
        label 'AGENT-1'
    }
    options{
        timeout(time: 30, unit: 'MINUTES')
        disableConcurrentBuilds()
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
    }
}