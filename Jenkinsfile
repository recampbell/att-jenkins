
node ("docker-cloud") {
    checkout scm
    docker.image("jess/zsh").inside {
        sh "ls -la"
        sh "zsh allthethings.sh"
    }
    
}

