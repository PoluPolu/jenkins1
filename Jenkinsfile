import java.io.File 
pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                script{
                
                def newFile = new File("/tmp/test.txt")
                newFile.write("teges szmeges")
		println	newFile.text
                }
            }
        }
		
		stage('Dir') {
            steps {
				script {
					// now you are on slave labeled with 'label'
					def workspace = WORKSPACE
					// ${workspace} will now contain an absolute path to job workspace on slave

					workspace = env.WORKSPACE
					// ${workspace} will still contain an absolute path to job workspace on slave

					// When using a GString at least later Jenkins versions could only handle the env.WORKSPACE variant:
					echo "Current workspace is ${env.WORKSPACE}"

					// the current Jenkins instances will support the short syntax, too:
					echo "Current workspace is $WORKSPACE"
                }
            }
          
        }
    }
}
