
node {
    withColor{
        try{
            stage('MVN'){
                sh "./mvnw clean package"
            }
        }
        finally {
            junit '**/target/surefire-reports/*.xml'
        }
    }
}

void withColor(Closure closure){
    ansiColor('xterm') {
        closure()
    }
}