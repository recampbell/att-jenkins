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
  }
}