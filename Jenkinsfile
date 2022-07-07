node {
  withCredentials([file(credentialsId: vault-pass, variable: 'FUCKFILE')]) {
        writeFile file: 'private.pem', text: readFile(FUCKFILE)
        
    }
}
