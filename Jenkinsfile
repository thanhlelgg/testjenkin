#!/usr/bin/env groovy

pipeline {
    agent {label 'slave1'}

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh "chmod 777 ./sendmail.py"
                sh "python sendmail.py"
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}

