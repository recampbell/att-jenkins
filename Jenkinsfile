
node ("mac") {
    checkout scm
    sh "bash allthethings.sh | tee output.file"
    archive "output.file"
}
