# **`Managing Docker Containers`**
===

## Run a Container
```bash
docker run [OPTIONS] IMAGE [COMMAND] [ARG...]
```
Run a command in a new container.

## List Running Containers
```bash
docker ps
```
List running containers.

## List All Containers
```bash
docker ps -a
```
List all containers (running and stopped).

## Stop a Container
```bash
docker stop CONTAINER [CONTAINER...]
```
Stop one or more running containers.

## Start a Stopped Container
```bash
docker start CONTAINER [CONTAINER...]
```
Start one or more stopped containers.

## Create a new image from a container
```bash
docker commit [OPTIONS] CONTAINER [REPOSITORY[:TAG]]
```
Save the current state of a container as a new image

## Restart a Container
```bash
docker restart CONTAINER [CONTAINER...]
```
Restart one or more containers.

## Remove a Container
```bash
docker rm CONTAINER [CONTAINER...]
```
Remove one or more containers.

## Inspect Container
```bash
docker inspect CONTAINER
```
Display detailed information on one container.

## Execute Command in a Running Container
```bash
docker exec [OPTIONS] CONTAINER COMMAND [ARG...]
```
Run a command in a running container.

## Attach to a Running Container
```bash
docker attach CONTAINER
```

Attach local standard input, output, and error streams to a running container.

## Logs of a Container
```bash
docker logs [OPTIONS] CONTAINER
```
Fetch the logs of a container.

## Copy Files or Folders from/to a Container
```bash
docker cp [OPTIONS] CONTAINER:SRC_PATH DEST_PATH
docker cp [OPTIONS] SRC_PATH CONTAINER:DEST_PATH
```
Copy files or folders between a container and the local filesystem.
