node {
          stage('Deploy'){
      agent any
      steps{
sudo docker -H tcp://0.0.0.0:4243 build -t webimage:$BUILD_NUMBER .
sudo docker container run -itd --name webserver$BUILD_NUMBER -p 8080 webimage:$BUILD_NUMBER'''
      }
 }
  }
