pipeline {
	agent any
	stages {
	    stage('Checkout') {
	        steps {
			checkout scm			       
		      }}
		stage('Build') {
	           steps {
			  sh '/home/akshay/Downloads/Software/apache-maven-3.9.6/bin/mvn install'
	                 }}
		stage('Deployment'){
		    steps {
			script {
			 if (env.BRANCH_NAME == 'master') 
                        {
                        echo 'Hello from main branch'
                        }
                    	if (env.BRANCH_NAME == 'dev') 
                        {
                        echo 'Hello from dev branch'
                        }
                    	else {
                        sh "echo 'Hello from ${env.BRANCH_NAME} branch!'"
                        }
                    
			}}}}	
}
