
node ("docker-cloud") {
    checkout scm
    def attImage = docker.build 'allthethings:snapshot'
    
    attImage.inside {
        sh 'ls -l /'
        sh 'zsh /allthethings.sh'
    }
    
}

