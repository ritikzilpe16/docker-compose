- docker network create mynet
- docker network ls
- docker run -d --name web1 --network mynet nginx:alpine
- docker run -d --name web2 --network mynet nginx:alpine
- verify the container runs at : docker ps 
if not:
docker ps -a
docker log <container>
- docker exec -it web2 sh
- inside the shell: run
- apk add --no-cache curl
- curl http://web1