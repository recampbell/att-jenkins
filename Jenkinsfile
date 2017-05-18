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
        echo 'Deploying'
        sleep 10
      }
    }

    stage('archive') {
      steps {
        archiveArtifacts 'allthethings.sh'
      }
    }
 }
}