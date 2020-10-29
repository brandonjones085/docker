pipeline {
    agent any

    stages {

      stage('Clone repository') {

        steps {
              checkout scm 
            }
      }
        stage('build') {
            steps {
              app = docker.build("getintodevops/hellonode")
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