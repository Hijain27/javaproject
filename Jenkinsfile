def service = ServiceHelper.getService("${name}")
pipeline {
    agent any
	    environment {
        ENV1_DEPLOY_BRANCH= 'main'
        ENV2_DEPLOY_BRANCH= 'dev'
        MASTER_MAJOR_REV= "4"
        }
	
    stages {
        stage('Checkout') {
            steps {
            echo "checking out from git"
            script{
            pipelineconfig_chkout()
            checkout scm
            sname = name.toLowerCase()
            }
      }
}
}
}

def pipelineconfig_chkout() {
        checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'GIT-HUB-CRED', url: 'https://github.com/Hijain27/javaproject.git']]])
    }
