
pipeline {
  triggers {
    cron ('H */4 * * 1-5')
  }
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
    stage('archive') {
      steps {
        archiveArtifacts 'allthethings.sh'
      }
    }
  }
  post {
    always {
       echo "This will always be printed"
    }
  }
}
