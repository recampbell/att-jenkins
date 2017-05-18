pipeline {
  agent {
    docker {
      image 'jess/zsh'
    }
    
  }
  stages {
    stage('compile') {
      steps {
        sh 'zsh -n allthethings.sh'
      }
    }
    stage('test') {
      steps {
        sh 'zsh allthethings.sh'
      }
    }
  }
}