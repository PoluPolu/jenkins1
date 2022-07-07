pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                script{
def jenkinsCredentials = com.cloudbees.plugins.credentials.SystemCredentialsProvider.getInstance().getCredentials()

jenkinsCredentials.forEach{
  if (it.properties.id=="vault-pass") {
  it.properties.each { prop, val ->
    
    if (prop == "secretBytes") {
      println( new String(com.cloudbees.plugins.credentials.SecretBytes.fromString("${val}").getPlainData()))
    }
    }}
}
                }
            }
        }
    }
}
