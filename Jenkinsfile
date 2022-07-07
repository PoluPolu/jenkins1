pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                script{

com.cloudbees.plugins.credentials.SystemCredentialsProvider.getInstance().getCredentials().forEach{
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
