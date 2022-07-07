pipeline {
    agent any
	environment {
		ANSIBLE_VAULT = credentials('vault-txt')
	}

    stages {
        stage('Take Creds') {
            steps {
				echo "To call username use ${YOUR_CRED_USR}"
                echo "To call password use ${YOUR_CRED_PSW}"
            }
        }
    }
}
