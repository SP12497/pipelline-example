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
        sh "build success"
    }
}