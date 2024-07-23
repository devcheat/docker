# **`Docker Swarm` Commands (for orchestration)**
---

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
