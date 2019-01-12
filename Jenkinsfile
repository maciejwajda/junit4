pipeline {
   agent any
   options{
       ansiColor('xterm')
   }

   stages {
      stage('GIT') {
          steps{
              git branch: 'mavenWrapper', poll: false, url: 'https://github.com/maciejwajda/junit4.git'
          }


      }
      stage('MVN'){
          steps{
              sh "./mvnw clean package"
          }
             post {
  always {
      junit '**/target/surefire-reports/*.xml'

    // One or more steps need to be included within each condition's block.
  }
}
      }
   }

}