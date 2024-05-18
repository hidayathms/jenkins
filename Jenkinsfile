
// refernce document https://www.jenkins.io/doc/book/pipeline/syntax/#environment

pipeline {
    agent any
    environment {
        ENV_URL="globalvar.google.com"   // pipeline global variable
    }
    stages {
        stage ('Name of the stage -1') {
           steps{
            sh "echo Name of the varialble is ${ENV_URL}"
           }
        }
        stage ('Name of the stage -2') {
            environment{
                ENV_URL="localvar.google.com"
            }
           steps{
            sh "echo Name of the varialble is ${ENV_URL}"
            sh "echo step2"
            sh "echo step3"
           }
        }
        stage ('Name of the stage -3') {
           steps{
            sh "echo step1"
            sh "echo step2"
            sh "echo step3"
           }
        }
    }
}