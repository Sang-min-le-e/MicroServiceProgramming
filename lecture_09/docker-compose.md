# docker-compose practice Command
docker compose up -d
docker-compose config
docker container ls -a 
docker image ls
docker stats
docker-compose down

# Manager & Workers (Ubuntu)
- docker-compose.yml
docker compose up -d
docker container ls
curl http://localhost:8001
curl http://localhost:8002
docker container exec -it {manager container ID} /bin/bash
apt-get update
apt-get upgrade
apt-get -y install curl
curl http://worker1:80
curl http://worker2:80

# Manager & Workers (Alpine)
- docker-compose.yml
docker compose up -d
docker container ls
curl http://localhost:8001
curl http://localhost:8002
docker container exec -it {manager container ID} /bin/sh
apk add curl
curl http://worker1:80
curl http://worker2:80
docker compose down

docker compose up -d --scale manager=4
docker container ls -a
docker compose ps
docker compose logs
docker compose down

docker compose run -p 9998:80 -d worker1

