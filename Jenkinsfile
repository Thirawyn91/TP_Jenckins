node {
              stage('Clone repository') {
        /* Let's make sure we have the repository cloned to our workspace */

        checkout scm
    }
          stage('Deploy'){
      agent any
      steps{
sh sudo docker build -t "webimage:$BUILD_NUMBER" .
sh docker container run -itd --name webserver$BUILD_NUMBER -p 8080 "webimage:$BUILD_NUMBER"
      }
 }
  }
