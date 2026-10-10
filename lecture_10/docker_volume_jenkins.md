# Docker Volume & jenkins practice
docker volume --help
docker volume create myvol-1
docker volume ls
docker volume inspect myvol-1

docker pull jenkins/jenkins"lts
docker run -p 8080:8080 -p 50000:50000 -v myvol-1 /var/jenkins_home jenkins/jenkins:lts

---
# Jenkins Upgrade
docker container stop {jenkins container ID}
docker volume ls
docker volume inspect myvol-1

docker run --name jenkins-production --detach -p 8080:8080 -v myvol-1:/var/jenkins_home jenkins/jenkins:lts
---

# Excute another Jenkins
docker run --name jenkins-production-copy --detach -p 50001:50000 -p 8081:8080 -v myvol-1:/var/jenkins_home jenkins/jenkins:lts

# Remove Volume
docker volume ls
docker volume rm {volume name}
docker volume prune



