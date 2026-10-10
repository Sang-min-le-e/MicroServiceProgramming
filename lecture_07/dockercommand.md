# Test-Drive: Executation of Dockerfile
docker build -t myapp
docker run -it --rm --name py3 myapp

# Basic Command
docker pull
docker build
docker image ls
docker container run
docker container ls
docker container ls -a
docker container ls -a -q
docker container stop
docker container kill

# Information Command
docker --version
docker system info
docker system df
docker ps
docker stats
docker search

# Clean-up Command
docker umage rm -f
docker container rm -f
docker system prune
