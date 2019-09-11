pipeline {
    agent any 
    stages {
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
		libraryResource '/org/dcube/sample.txt'
            	bat "echo shared library"
		}
		}
		
        stage('Deploy') { 
            steps {
                bat "echo Deploy"
            }
        }
    }
}
