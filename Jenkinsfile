#!/usr/bin/env groovy

pipeline {
    agent {label 'slave1'}

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh "chmod 777 test/sendmail.py"
                sh "python test/sendmail.py"
            }
        }
        stage('Test') {
            when { branch 'master' }
            steps {
                echo 'Testing on master..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}

