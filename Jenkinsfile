#!/usr/bin/env groovy

pipeline {
    agent any
    
    node {
        checkout scm
        chmod 777 ./sendmail.py
        ./sendmail.py
    }

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
            steps {
                echo 'Deploying....'
            }
        }
    }
}

