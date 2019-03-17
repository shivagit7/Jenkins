
# Docker file for Jenkins Master Image

FROM jenkins/jenkins:latest

RUN /usr/local/bin/install-plugins.sh git mstest matrix-auth workflow-aggregator docker-workflow blueocean credentials-binding

ENV JENKINS_USER ts-tcs-admin
ENV JENKINS_PASS ts-tcs-password

# Skip initial setup
ENV JAVA_OPTS -Djenkins.install.runSetupWizard=false

COPY executors.groovy /usr/share/jenkins/ref/init.groovy.d/
COPY default-user.groovy /usr/share/jenkins/ref/init.groovy.d/
