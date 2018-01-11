#!/usr/bin/env groovy

pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            chmod 777 ./sendmail.py
            ./sendmail.py
            steps {
                echo 'Deploying....'
            }
        }
    }
}

