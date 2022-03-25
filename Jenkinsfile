pipeline {
 agent{label 'docker-slave'}
  stages {
    stage('Cloning Git') {
      steps {
        git([url: 'https://github.com/barathtech/movieapp.git', branch: 'main', ])
        sh ''' apt install docker.io -y '''
        }
    }
    stage('Building image') {
      steps{
        script {
          dockerImage = docker build.ubuntu
        }
      }
    }
  }
}
