pipeline{
    agent any
    tools{
        maven: "apache-maven-3.9.6"
    }
    environment{
        VERSION_NAME="1.34"
    }
    stages{
        stage("compile") {
            steps {
                sh "javac Main.java"
                sh 'echo "${VERSION_NAME}"'
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