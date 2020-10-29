pipeline {
    agent any

    stages {

      stage('Clone repository') {

        checkout scm
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