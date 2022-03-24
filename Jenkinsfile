pipeline {
  environment {
    imagename = "bk"
    dockerImage = ''
  }
  node('java-docker-slave'){ 
  stage('Cloning Git') {
      steps {
        git([url: 'https://github.com/barathtech/movieapp.git', branch: 'main', ])

      }
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
