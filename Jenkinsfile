
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
    stage ("test") {
      steps {
        sh 'zsh allthethings.sh'
      } 
    }
    stage ("deploy") {
      steps {
        sh 'zsh allthethings.sh'
	milestone 1
	lock "staging"
	milestone 2
        echo 'Deploying'
        sleep 60
      }
    }

    stage('archive') {
      steps {
        archiveArtifacts 'allthethings.sh'
      }
    }
 }
}