pipeline {
    agent any
	environment {
		ANSIBLE_VAULT = credentials('vault-txt')
	}

    stages {
        stage('Take Creds') {
            steps {
		echo "To call username use ${Id}"
                echo "To call password use ${Secret}"
            }
        }
    }
}
