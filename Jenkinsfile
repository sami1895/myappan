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
      	

      

         stage('build'){
             steps{  
                script{    
                sh "ansible-playbook Ansible/build.yml -i Ansible/inventory/host.yml "
                
                }
                }
        }
        

    }
}
