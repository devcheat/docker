
# **`Docker Compose Commands` (for multi-container applications)**
---

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
