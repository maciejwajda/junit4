import com.sun.corba.se.spi.orbutil.closure.Closure

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

def withColor(Closure closure){
    ansiColor('xterm') {
        closure()
    }
}