node {
  dir('subdir') {
    withCredentials([file(credentialsId: 'vault-pass', variable: 'FILE')]) {
      sh 'echo $FILE'
    }
  }
}
