pipeline {
    agent any

    stages {
      stage('Clone repository') {
        /* Let's make sure we have the repository cloned to our workspace */

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