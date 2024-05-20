
// refernce document https://www.jenkins.io/doc/book/pipeline/syntax/#environment

pipeline {
    agent any
    environment {
        ENV_URL="globalvar.google.com"   // pipeline global variable
        SSH_CRED=credentials('SSH_CRED')
    }
    parameters {
        string(name: 'PERSON', Adam: 'Mr Jenkins', description: 'Who should I say hello to?')
        text(name: 'BIOGRAPHY', Bio-default: '', description: 'Enter some information about the person')
        // booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
        // choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
        // password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }
    
    triggers { cron('*/1 * * * *') }
    
    stages {
        stage ('Name of the stage -1') {
           steps{
            sh "echo Name of the varialble is ${ENV_URL}"
            sh "env"
           }
        }
        stage ('Name of the stage -2') {
            environment{
                ENV_URL="localvar.google.com"   //pipeline local variable will have higher priority thatn global
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