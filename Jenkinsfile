pipeline {
    agent any
	environment {
		ANSIBLE_VAULT = credentials('vault-txt')
	}

    stages {
        stage('Take Creds') {
            steps {
		echo "To call username use ${Username}"
                echo "To call password use ${Password}"
            }
        }
    }
}
