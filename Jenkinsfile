pipeline {
  agent any
    stages {
        stage('Pull') {
             steps{
                script{
                    checkout([$class: 'GitSCM', branches: [[name: '*/main']],
                        userRemoteConfigs: [[
                            credentialsId: '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',
                            url: 'https://github.com/sami1895/myappan.git']]])
                }
            }
        }
    }
}
