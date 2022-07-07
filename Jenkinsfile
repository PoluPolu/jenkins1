pipeline {
   agent any
   stages {
       stage('write') {
           steps {
              
               dir('subdir') {
    withCredentials([file(credentialsId: 'vault-pass', variable: 'FILE')]) {
      sh 'echo $FILE'
    }
               script {
                   
                 
                  
                  def date = new Date()
                   def data = "Hello World\nSecond line\n" + date
                   writeFile(file: 'zorg.txt', text: data)
                   sh "ls -l"
               }
           }
       }
       stage('read') {
           steps {
               script {
                   def data = readFile(file: 'zorg.txt')
                   println(data)
               }
           }
       }
   }
}
