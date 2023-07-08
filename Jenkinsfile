pipeline {
  agent any
    stages {
        stage('Pull') {
             steps{
                script{
                    checkout([$class: 'GitSCM', branches: [[name: '*/main']],
                        userRemoteConfigs: [[
                            credentialsId: '22e9a5e1-7abb-4428-8021-b9242c527392',
                            url: 'https://github.com/sami1895/myappan.git']]])
                }
            }
        }
    }
}
