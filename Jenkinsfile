node {
  dir('subdir') {
    withCredentials([file(credentialsId: 'secret', variable: 'FILE')]) {
      sh 'use $FILE'
    }
  }
}
