node {
              stage('Clone repository') {
        /* Let's make sure we have the repository cloned to our workspace */

        checkout scm
    }
          stage('Deploy'){
      agent any
      steps{
sh sudo docker build . -t webimage
      }
 }
  }
