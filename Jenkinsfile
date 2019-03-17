

node('docker') {

    stage 'Checkout'
        checkout scm

    stage 'Docker_Images_Before_Build'
        echo "Listing Docker Images Before Build"
        sh "docker images"

    stage 'Build Docker Images'
    sh "docker build -t sample:B${BUILD_NUMBER} -f /Build/sample1/Dockerfile"

    stage 'Docker_Images_After_Build'
        echo "Listing Docker Images After Build"
        sh "docker images"
}
