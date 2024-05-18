
// refernce document https://www.jenkins.io/doc/book/pipeline/syntax/#environment

pipeline {
    agent any
    environment {
        ENV_URL="pipeline.google.com"
    }
    stages {
        stage ('Name of the stage -1') {
           steps{
            sh "Name of the varialble is ${ENV_URL}"
           }
        }
        stage ('Name of the stage -2') {
           steps{
            sh "echo step1"
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