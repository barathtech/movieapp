pipeline {
  environment {
    imagename = "bk"
    dockerImage = 'ubuntu'
  }
agent {label 'java-docker-slave'}
  stages {
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
