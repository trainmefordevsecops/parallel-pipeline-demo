pipeline {
    agent none

    stages {
        stage('Build and run') {
          parallel {
            stage('master-agent-pipeline') {
              agent {label 'master'}
              stages{
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
	       }
              }
            stage('ubuntu-agent-pipeline') {
              agent {label 'ubuntu'}
              stages{
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
               }
              }
             }
            }
           }
          }
