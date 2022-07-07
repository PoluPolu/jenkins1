pipeline {
    agent any
	environment {
		ANSIBLE_VAULT = credentials('vault-txt')
	}

    stages {
		stage('string (secret text)') {
			  steps {
				script {
				  withCredentials([
					file(
					  credentialsId: 'vault-pass',
					  variable: 'ENV_FILE')
				  ]) {
					 sh "cp \$ENV_FILE /tmp/my-public-key.der"
				  }
				}
			  }
			}
    }
}
