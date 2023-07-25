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
                    sh "npm install"
                }
            }
        }


	
stage("test"){
      steps {
        echo "test stage"
      }
    }
	
     
     

}
}	
