

node('docker') {

    stage 'Checkout'
        checkout scm

    stage 'Present Working Directory'
        sh "pwd"
        sh "ls -la"

    stage 'Docker_Images_Before_Build'
        echo "Listing Docker Images Before Build"
        sh "docker images"

    stage 'Build Docker Images'

    sh "pwd"
    sh "ls -la"
    sh "docker build -t sample:B${BUILD_NUMBER} ./Build/Sample1/Dockerfile ."

    stage 'Docker_Images_After_Build'
        echo "Listing Docker Images After Build"
        sh "docker images"
}
