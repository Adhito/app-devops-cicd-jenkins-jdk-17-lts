# Jenkins JDK 17 LTS
Guide on how to deploy Jenkins JDK 17 LTS with Container Engine (Docker/Podman)

[ ## ]  Install Jenkins JDK 17 LTS

## Pull the Jenkins Image
docker pull jenkins/jenkins:2.426.2-lts-jdk17

## Run the Jenkins Container using default param
docker run -d -p 8080:8080 -p 50000:50000 -v jenkins_home:/var/jenkins_home jenkins/jenkins:lts-jdk17

## Run the Jenkins Container with WSL2 mount on C: Drive
docker run -d -p 8080:8080 -p 50000:50000 -v /mnt/c/ENV_Application_Jenkins_JDK_17_LTS:/var/jenkins_home --name jenkins-lts-jdk17-ver-2.426 jenkins/jenkins:2.426.2-lts-jdk17 