node {
    def app

    stage('Clone repository') {
        /* Check out repo */

        checkout scm
    }

    stage('Build image') {
        /* builds image and stores in app variable */
  image
       app = docker.build("brandonjones085/test")
    }

    stage('Test image') {
  
         /* Placeholder for unit tests*/
        app.inside {
          passed"'
        }   sh 'echo "Tests
    }

    stage('Push image') {
         /* Uses git credentials to push to dockerhub with latest tag*/

        docker.withRegistry('https://registry.hub.docker.com', 'git') {
            app.push("${env.BUILD_NUMBER}")
            app.push("latest")
        }
    }
}