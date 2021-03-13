# Docker-Intro -  Getting Started with Docker

### To get Docker Container Repo from Docker (To download)

```
docker pull <image>
```
or 
```
docker run <image>:<version>
```

If version is not provided, the docker fetched the image with the latest version.
Also, if the docker does not find any image locally, it will then download from the dockerhub library

All the layers are seperately downloaded - if there are seperate versions of same container - then the same layers won't be downloaded again!

As soon as it downloads it, it will start running it.

Docker containers can be easily terminated by pressing Ctrl+C

#### To run the container in a detached mode:
```
docker run -d <imagename>
```
This command will return the container ID.
```
docker run -d --name <name of your choice> <image name>
```
#### To restart the docker container:
```
docker stop <container ID>
````
And then start that container using this command:
```
docker start <container ID>
```
  
Also Docker run is to create a new container, and docker start starts the already created stopped container!

#### To Run and Bind a container to host port
```
docker run -p<hostport>:<containerPort> <imagename>
```

### To check all the Running Container
```
docker ps
```
Will give out the running container, and the container ID

```
docker ps -a 
```
Will give all the containers, stopped and running
Image and Container -
Image - Actual Package/Artifact
Container - when the image is pulled and starts, then it is running, then it is a container!

### To check all the images installed in Docker
```
docker images
```

This command lists down all the imges with Name, Tag, Image ID and Size

Tags are basically versions

### Debugging Containers

```
docker logs <container Id>
    or
docker logs <container name>
```

To get the terminal of the running container:
```
docker -exec -it <container ID> /bin/bash
```
You will enter as a root user and can make any number of changes! And then exit the terminal using exit



