import java.io.File 
pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                script{
                String fileName = "./test.txt"
                def newFile = new File(fileName)
                newFile.write("teges szmeges2")
                }
            }
        }
		

    }
}
