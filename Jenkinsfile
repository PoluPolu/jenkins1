void prepareVaultfile(String fileName) {
	Map configMap = [:]
	def props = readProperties file: fileName
}


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
					prepareVaultfile(ENV_FILE)
				  }
				}
			  }
			}
    }
}
