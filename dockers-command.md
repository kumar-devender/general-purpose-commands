#### List containers
```
docker ps -a
```
#### Remove containers
```
docker rm <container-id>
```
docker run -it helloWorld
docker pull tomcat
docker image prune -a
docker container prune | This will remove all stopped containers
docker image prune  | This will remove all dangling images
docker network prune
docker-compose up --build
docker-compose up
docker-compose down
docker rmi $(docker images -a -q)
docker rmi $(docker images -a -q) -f
