
node ("mac") {
    checkout scm
    sh "bash allthethings.sh | tee output.file"
    stash includes:"allthethings.sh", name:"script"
}

parallel block1: {
    node ("mac") {
        sleep 20
        unstash "script"
        sh "sh allthethings.sh"        
    }

}, block2: {
    node ("mac") {
        sleep 20
        unstash "script"
        sh "sh allthethings.sh"        
    }
}
