run docker container with Jenkins image as a demon

docker run -d -p 80:8080 -v $HOME/jenkins_home:/var/jenkins_home --name jenkins-master jenkins:latest
