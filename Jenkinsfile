
node ("docker-cloud") {
    checkout scm
    docker.image("jess/zsh").inside {
        sh "zsh allthethings.sh"
    }
    
}

