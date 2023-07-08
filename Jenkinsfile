pipeline {
  agent any
    stages {
        stage('Pull') {
             steps{
                script{
                    checkout([$class: 'GitSCM', branches: [[name: '*/main']],
                        userRemoteConfigs: [[
                            credentialsId: 'c5d71fe3-c5c5-4e22-849e-4f0b3eaa1e59',
                            url: 'https://github.com/sami1895/myappan.git']]])
                }
            }
        }
