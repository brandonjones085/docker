pipeline {
    agent any

    stages {
      stage('Clone repository') {
        /* Let's make sure we have the repository cloned to our workspace */

        checkout scm
      }
        stage('Install') {
            steps {
              sh '''
                npm install --verbose -d 
                npm install --save classlist.js
                '''
                
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }

        stage('Build') {
            steps {
              sh '$(npm bin)/ng build --prod --build-optimizer'
                
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}