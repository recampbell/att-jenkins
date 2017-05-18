@Library('github.com/recampbell/zsh-pipeline')
import recampbell.zsh.Zsh

pipeline {
  agent {
    docker {
      image 'jess/zsh'
    }
    
  }
  stages {
    stage('compile') {
      steps {
	 testZsh 'allthethings.sh'
      }
    }
    stage('test') {
      steps {
        parallel(
          "test": {
            sh 'zsh allthethings.sh'
            
          },
          "deploy": {
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