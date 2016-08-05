
node ("docker-cloud") {
    checkout scm
    sh "ps -ef"
    docker.image("jess/zsh").inside {
        sh 'ps -ef'
        sh "ls -la"
        sh "zsh allthethings.sh"
    }
    
}

