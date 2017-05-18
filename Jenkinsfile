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
        parallel(
          "test": {
            sh 'zsh allthethings.sh'
            
          },
          "deploy": {
	    milestone 1
            echo 'Deploying'
            sleep 10
            
          }
        )
      }
    }
    stage('archive') {
      steps {
        archiveArtifacts 'allthethings.sh'
      }
    }
  }
}