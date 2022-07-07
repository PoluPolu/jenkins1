node {
  withCredentials([file(credentialsId: 'vault-pass', variable: 'FILE')]) {
    dir('subdir') {
      sh 'touch $FILE'
    }
  }
}
