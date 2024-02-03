# Jenkins 

## Run jenkins using docker image
```
docker run -p 8080:8080 -p 50000:50000 --restart=on-failure -v jenkins_home:/var/jenkins_home jenkins/jenkins:lts-jdk17
docker ps
docker logs <jenkins_container_id/name>
docker volume inspect jenkins_home
```
Go to Volume in Docker desktop.  
Open jenkins_home volume.  
Save `/var/jenkins_home/secrets/initialAdminPassword` file in system.  
Open file in text editor to see initial password.  
Open `localhost:8080` to configure jenkins.

### Explore Jenkins container - 
```
docker ps
docker exec <jenkins_container_id/name> ls
docker exec -it -u root <jenkins_container_id/name> /bin/bash
apt-get update
exit
```
![Jenkins Container](./images/jenkins-container-docker-desktop.png)

### Create first job

#### Using Freestyle project
![Jenkins Freestyle project](./images/jenkins-freestyle-job-project.png)
![Jenkins Freestyle Job Output](./images/jenkins-freestyle-job-output.png)

#### Using Pipeline - Script


#### Using Pipeline - Jenkinsfile


---

## References - 
[Jenkins documentation](https://www.jenkins.io/doc/)  
[Official Jenkins Docker image](https://hub.docker.com/r/jenkins/jenkins)  
[Jenkins Docker image documentation](https://github.com/jenkinsci/docker/blob/master/README.md)

--- 

## Todo

- setup jenkins server in local at jenkins-server.com
- checkout git repository and compile it