pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
                fileExists 'pp.txt'
            }
        }
        stage('Build') {
            steps {
                echo 'Building'
                fileExists 'pp.txt'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying'
            }
        }    
        stage('Test') {
            steps {
                echo 'Testing'
            }
        }    
        stage('Release') {
            steps {
                echo 'Releaseing'
            }
        }    
    }
}
