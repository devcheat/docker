# **`Managing Docker Networks`**
---

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
