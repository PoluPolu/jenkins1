import java.io.File 
pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                script{
                
                def newFile = new File("env.WORKSPACE/test.txt")
				
                newFile.write("teges szmeges")
                }
            }
        }
		

    }
}
