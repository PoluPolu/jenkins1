pipeline {
    agent any
    stages {
		stage('string (secret text)') {
			  steps {
				script {
					
				  withCredentials([
					file(
					  credentialsId: 'vault-pass22',
					  variable: 'ENV_FILE')
				  ]) {
					  String fileName = env.WORKSPACE + "/test22.txt"
					 sh "cp \$ENV_FILE $fileName"
				  }
				}
			  }
			}
    }
}
