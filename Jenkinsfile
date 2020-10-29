pipeline {
    agent any

    stages {
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