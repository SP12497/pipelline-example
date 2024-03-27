pipeline{
    agent any
    stages{
        stage("compile") {
            steps {
                sh "javac Main.java"
            }
        }
        stage("run"){
            steps {
                sh "java Main"
            }
        }
    }

    post{
        always {
            sh "echo always print"
        }
        success {
            sh "build success"
        }

        failure{
            sh "echo failure print"
        }
    }
}