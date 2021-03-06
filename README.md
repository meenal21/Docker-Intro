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

As soon as it downloads it, it will start running it

### To check all the Running Container
```
docker ps
```

Will give out the running container, and the container ID

Image and Container -
Image - Actual Package/Artifact
Container - when the image is pulled and starts, then it is running, then it is a container!

