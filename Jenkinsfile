pipeline {
  agent any
  stages {
    stage('compile') {
      steps {
        sh 'bash -n allthethings.sh'
      }
    }
    stage('test') {
      steps {
        sh 'sh allthethings.sh'
      }
    }
    stage('archive') {
      steps {
        archiveArtifacts 'allthethings.sh'
      }
    }
  }
}