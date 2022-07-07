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
					string(
					  credentialsId: 'vault-txt',
					  variable: 'joke')
				  ]) {
					print 'joke=' + joke
					print 'joke.collect { it }=' + joke.collect { it }
				  }
				}
			  }
			}
    }
}
