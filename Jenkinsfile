pipeline {
    agent any
    stages {
		stage('string (secret text)') {
			  steps {
				
				  step {	
				  withCredentials([
					file(
					  credentialsId: 'vault-pass22',
					  variable: 'ENV_FILE')
				  ]) {
					 String fileName = env.WORKSPACE + "/test22.txt"
					 sh "rm -f $fileName"
					  sh "cp -r \$ENV_FILE $fileName"
					  sh "chmod 444 $fileName
				  } 
				  
				}
			  }
			}
    }
}
