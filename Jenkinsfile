pipeline {
    agent any 
    stages {
	    
	@Library('jenkinsLibrary')_
        stage('Build') { 
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/apurva1j/pipelineDemo.git']]])
            }
        }
        stage('Test') { 
            steps {
                bat "echo Test"
            }
        }
	stage('sharedLib') {
	steps {
    	HelloWorld('helloooo world')
   	 }

	}	
		
        stage('Deploy') { 
            steps {
                bat "echo Deploy"
            }
        }
    }
}
