**`Docker cli`**
===

# Docker Management Commands
## Docker Version Check
```bash
docker --version
```
Display Docker version information.

## Docker Info
```bash
docker info
```
Display system-wide Docker information.
 
## Docker Help
```bash
docker --help
```
Display help information on Docker commands.

# Managing Docker Containers

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

# Managing Docker Images
## List Images
```bash
docker images [OPTIONS] [REPOSITORY[:TAG]]    
```
List images.

### Pull an Image
```bash
docker pull NAME[:TAG|@DIGEST]
```
Pull an image or a repository from a registry.

## Remove an Image
```bash
docker rmi IMAGE [IMAGE...]    
```
Remove one or more images.

## Inspect Image
```bash
docker image inspect NAME[:TAG|@DIGEST]
```
Display detailed information on one or more images.

## Tag an Image
```bash
docker tag SOURCE_IMAGE[:TAG] TARGET_IMAGE[:TAG]
```
Create a tag TARGET_IMAGE that refers to SOURCE_IMAGE.

## Build an Image from Dockerfile
```bash
docker build [OPTIONS] PATH | URL | -
```
Build an image from a Dockerfile.

## Push an Image to a Registry
```bash
docker push NAME[:TAG]
```
Push an image or a repository to a registry.

# Managing Docker Networks
## List Networks
```bash
docker network ls
```
List networks.

## Create a Network
```bash
docker network create [OPTIONS] NETWORK
```
Create a network.

## Inspect Network
```bash
docker network inspect NETWORK [NETWORK...]
```
Display detailed information on one or more networks.

## Connect a Container to a Network
```bash
docker network connect [OPTIONS] NETWORK CONTAINER
```
Connect a container to a network.

## Disconnect a Container from a Network
```bash
docker network disconnect [OPTIONS] NETWORK CONTAINER
```
Disconnect a container from a network.

# Managing Docker Volumes
## List Volumes
```bash
docker volume ls
```
List volumes.

## Create a Volume
```bash
docker volume create [OPTIONS] [VOLUME]
```
Create a volume.

## Inspect Volume
```bash
docker volume inspect [VOLUME...]
```
Display detailed information on one or more volumes.

## Remove a Volume
```bash
docker volume rm VOLUME [VOLUME...]
```

Remove one or more volumes.

# Docker Compose Commands (for multi-container applications)

## Start Services
```bash
docker-compose up [SERVICE...]
```
Build and start containers.

## Stop Services
```bash
docker-compose down
```
Stop and remove containers, networks, images, and volumes.

## List Services
```bash
docker-compose ps
```
List containers.

## View Logs
```bash
docker-compose logs [SERVICE...]
```
View output from containers.

## Execute Command in a Service Container
```bash
docker-compose exec [SERVICE] COMMAND [ARG...]
```
Run a command in a running service container.

# Docker Swarm Commands (for orchestration)
## Initialize Swarm
```bash
docker swarm init [OPTIONS]
```
Initialize a swarm.

## Join Swarm as a Worker
```bash
docker swarm join [OPTIONS] HOST:PORT
```
Join a swarm as a worker node.

## Join Swarm as a Manager
```bash
docker swarm join-token [OPTIONS] [TOKEN]
```
Manage join tokens.

## Deploy a Stack
```bash
docker stack deploy [OPTIONS] STACK
```
Deploy a new stack or update an existing stack.

## List Services in a Swarm
```bash
docker service ls
```
List services in the swarm.

# Docker System Management
## Remove Unused Data
```bash
docker system prune [OPTIONS]
```
Remove unused data.

## Monitor Docker's Events
```bash
docker events [OPTIONS]
```
Get real-time events from the server.

# Docker Registry and Repository
## Login to Docker Registry
```bash
docker login [OPTIONS] [SERVER]
```
Log in to a Docker registry.

## Logout from Docker Registry
```bash
docker logout [SERVER]
```
Log out from a Docker registry.

## Search for Docker Images
```bash
docker search [OPTIONS] TERM
```
Search Docker Hub for images.


# How to Push a Docker Image
## 1. Tag the Docker Image
Before pushing the image, you need to tag it with the repository name and optionally a tag. The tag helps identify the specific version of the image.
```bash
docker tag IMAGE_ID REPOSITORY:TAG
```
- IMAGE_ID: The ID of the image you want to push. You can get this from docker images.
- REPOSITORY:TAG: The repository name and tag you want to assign to the image.

For example, tagging an image for Docker Hub:
```bash
docker tag my-image:latest username/my-repo:latest
```
Replace my-image:latest with your local image name and tag, and username/my-repo:latest with your Docker Hub repository and tag.

## 2. Login to Docker Registry
If you are pushing to Docker Hub or a private registry, log in using docker login:
```bash
docker login
```
Follow the prompts to enter your Docker Hub or registry username and password.

## 3. Push the Docker Image
Once logged in, you can push the tagged image to the registry:
```bash
docker push REPOSITORY:TAG
```
For example, to push the image username/my-repo:latest to Docker Hub:
```bash
docker push username/my-repo:latest
```
This command uploads the image layers to the specified Docker registry.

## 4. Verify the Push
After the push completes, you can verify that the image is available in the registry by searching for it on Docker Hub or using docker search if it's a private registry. Example Workflow Here’s a complete example of pushing a Docker image to Docker Hub:


## Additional Considerations
- **Image Naming:** Ensure your repository and tag names are meaningful and follow best practices.
- **Versioning:** Use appropriate tags (latest, version numbers, etc.) to manage different versions of your images.
- **Security:** Keep your Docker registry credentials secure and avoid hardcoding them in scripts.

By following these steps, you can effectively push your Docker images to a registry for distribution and deployment.
