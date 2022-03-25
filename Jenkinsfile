pipeline {
 agent 
  stages {
    stage('Cloning Git') {
      steps {
        git([url: 'https://github.com/barathtech/movieapp.git', branch: 'main', ])
        sh''' apt install nodejs -y'''
        sh'''apt install docker -y'''
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
