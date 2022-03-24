node 'java-docker-slave'{ 
  stage('Cloning Git') {
        git 'https://github.com/barathtech/movieapp.git'
      }
    stage('Building image') {
      steps{
        script {
          dockerImage = docker.build imagename
        }
      }
    }
  }
}
