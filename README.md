PRINCIPAIS COMANDOS DE DOCKER

docker container run <name of the image> -> run the container from the image

docker ps -a-> list all open containers

docker container ls -a | grep <name of the image> -> filter the list of containers with that image

docker container rm <name or id of container> -> deletes container

docker image rm <name or id of image> -> deletes image

docker rmi $(docker images -a -q) -> deletes all images

docker container prune -> deletes all containers

docker image prune -> delete not named and not used images

docker system prune -> delete almost everything

docker image pull <name of image> -> downloads the image without running it

docker run -d <name of the container> -> starts a container running in the background

docker container stop <name of the container> -> stops a running container

docker container rm --force <name of the container> -> force the remove of the container

docker container exec -it <name of the container> -> Executes a command inside the container

docker kill <name of container> -> is the same as docker container rm --force <name of the container>

docker start <name of container> -> starts closed container

docker cp <file> <container name:<path>> -> copy a file to a container

docker diff -> see the history of changes in the container

docker commit <name of container> <new name of image> -> add a new layer on top of the image of an old image

docker build -t <name> -f Dockerfile.<any name> (.<local>) -> Create distinct Dockerfiles under same project directory

docker run -v "$(pwd)</any archive or nothing>:<way of the container>" <image name> -> share the file in the container with the host machine

docker run -p <port host>:<port container> <name of image> -> publish a port of a container to the internet

