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
      	stage('Install') {
             steps{
                script{
                    sh "sudo npm install"
                }
            }
        }

      

         stage('build'){
             steps{  
                script{    
                sh "ansible-playbook Ansible/build.yml -i Ansible/inventory/host.yml "
                
                }
                }
        }
        

    }
}
