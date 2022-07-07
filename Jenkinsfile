pipeline {
    agent any
    stages {
		stage('string (secret text)') {
			  steps {
				script {
					String fileName = env.WORKSPACE + "/test22.txt"
				  withCredentials([
					file(
					  credentialsId: 'vault-pass22',
					  variable: 'ENV_FILE')
				  ]) {
					 sh "cp \$ENV_FILE $fileName"
				  }
				}
			  }
			}
    }
}
