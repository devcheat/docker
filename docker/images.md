# **`Managing Docker Images`**
---

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
