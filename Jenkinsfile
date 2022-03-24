pipeline {
  environment {
    imagename = "bk"
    dockerImage = ''
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
          dockerImage = ubuntu.build imagename
        }
      }
    }
  }
}
