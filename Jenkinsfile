node {
  dir('subdir') {
    withCredentials([file(credentialsId: 'vault-pass', variable: 'FILE')]) {
      sh 'use $FILE'
    }
  }
}
