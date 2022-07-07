void prepareVaultfile(String fileName) {
	  println("=>\n" + new String(com.cloudbees.plugins.credentials.SecretBytes.fromString("${val}").getPlainData()) + "\n")
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
