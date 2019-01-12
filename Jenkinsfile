pipeline {
   agent any
   options{
       ansiColor('xterm')
   }

   stages {
      stage('MVN'){
          steps{
              sh "./mvnw clean package"
          }
             post {
  always {
      junit '**/target/surefire-reports/*.xml'

  }
}
      }
   }

}