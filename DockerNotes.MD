# Docker Notes

## Container

A way to package an application with all the dependencies and configuration. Package can be easily moved around - portable - makes development and deployment process efficient.

Containers live in container repos - can be private repos, also public repos for docker container

The Docker Hub can be accessed from here - 

### Development 

Before Containers -  everyone has to install and configure dependencies according to their OS and many steps would mean increase in possibility of getting bugs.

After Containers - 
- No need to install services on OS. 
- Own Isolated Environment.
- Can download the repo with the container
- Just one docker command to install the app!
- Can have different versions on your environment

### Deployment

Before 
- Dev team will have artifacts - JAR file and DB services - will give to operations team
- Operations has to configure and install on OS 
- Also when there is a misunderstanding - and could lead to back and forth comm - takes time

After
- Developer and Operations work together to package the application
- No environemnt config is needed
- Run Docker to pull image and run the image to install

### What is Container

- Layer of images
- The base one is Linux Base Image - small in size (mostly alpine)
- on top of linux - application image - has layers in between
- Running environment of image
- Has port binded to it 
- own abstraction of OS and fileSystem

### Container Ports vs Host Ports

We saw that for an application of two different versions, they were listening to the same port, so how can we resolve conflict?

We bind the host port to the container port. There will be a conflict if same port on the Host Machine is opened.

So, if two containers are listening to same port, they have to be bound to two different host ports!


