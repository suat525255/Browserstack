pipeline {
   agent any
   tools {nodejs "node"}

   stages {
      stage('setup') {
         steps {
            browserstack(credentialsId: 'testID-test-test-test-test') {
               // some example test commands ...
               sh 'npm install'
               sh 'node parallel.js'
            }
             // Enable reporting in Jenkins
             browserStackReportPublisher 'automate'
         }
      }
    }
  }
