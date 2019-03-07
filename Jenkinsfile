#!groovy


pipeline {
    agent any
    triggers { pollSCM('* * * * *') }
    stages {
        stage('Build proyecto-1') {
            when {
                changeset "proyecto-1/**"
            }
            steps {
                build 'proyecto-1'
            }
        }
        stage('Build proyecto-2') {
            when {
                changeset "proyecto-2/**"
            }
            steps {
                build 'proyecto-2'
            }
        }
    }
}