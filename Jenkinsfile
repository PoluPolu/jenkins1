pipeline {
    agent any
    environment { 
        CC = 'clang'
    }
    stages {
        stage('Example') {
            environment { 
                AN_ACCESS_KEY = credentials('PoluSecTxt') 
            }
            steps {
                sh 'printenv'
            }
        }
    }
}
