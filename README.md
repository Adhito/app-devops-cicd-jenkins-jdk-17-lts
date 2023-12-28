# Jenkins JDK 17 LTS
Guide on how to deploy Jenkins JDK 17 LTS with Container Engine (Docker/Podman)


## Pull the Jenkins Image (Jenkins JDK 17 LTS)
`docker pull jenkins/jenkins:2.426.2-lts-jdk17`


## Run the Jenkins Container using default param
`docker run -d -p 8080:8080 -p 50000:50000 -v jenkins_home:/var/jenkins_home jenkins/jenkins:lts-jdk17` 


## Run the Jenkins Container with WSL2 mount on C: Drive
`docker run -d -p 8080:8080 -p 50000:50000 -v /mnt/c/ENV_Application_Jenkins_JDK_17_LTS:/var/jenkins_home --name jenkins-lts-jdk17-ver-2.426 jenkins/jenkins:2.426.2-lts-jdk17` 


## Renaming the container 
`docker container rename {$CONTAINER_NAME} jenkins-lts-jdk17-ver-2.426`

## TODO
1. Steps on setting up the jenkins
2. setting first admin user
3. login
4. upload screenshots