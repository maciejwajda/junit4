
node {
    withConf{
        try{

            stage ('GIT'){
                git branch: 'mavenWrapper', poll: false, url: 'https://github.com/maciejwajda/junit4.git'
            }
            stage('MVN'){
                sh "./mvnw clean package"
            }
        }
        finally {
            junit '**/target/surefire-reports/*.xml'
        }
    }
}

void withConf(Closure closure){
    ansiColor('xterm') {
        timestamps(){
            closure.call()
        }
    }
}