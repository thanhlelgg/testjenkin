#!/usr/bin/env groovy

pipeline {
    agent {label 'slave1'}

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh "chmod 777 test\sendmail.py"
                sh "python test\sendmail.py"
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

