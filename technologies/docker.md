# docker
*6.8.2020, puzzle, bbt session 2 bim raffi*

according to wikipedia:
> an open-source project that automates the deployment of software applications inside containers by providing an additional layer of abstraction and automation of OS-level virtualization on Linux.

Docker is a tool that allows to easily deploy an application in a container. Key is that one can package an appliation with all of its dependencies into a **standardized unit**.

## links
- Tutorial: [https://docker-curriculum.com/](https://docker-curriculum.com/)
- Getting Started: https://docs.docker.com/get-started/
- DockerHub: [https://hub.docker.com/](https://hub.docker.com/)


## containers

Industry standard is to use VM, but they have the downside of great computational overhead spent virtualizing hardware for a guest OS.

Containers leverage the low-level mechanics of the host operating system. Most of the isolation provided at fraction of computing power.


## command list
- `$ docker images` list all images
- `$ docker run [imagename]` find image, load up container and exit again
- `$ docker run -it [imagename] sh` find image, load up container and attach to interactive console
  - `--rm` ... and remove after exited
  - `-d` ... and detach terminal
  - `-P` ... and publish all ports to random ports
  - `-p [external_port]:[internal_port]` ... and specify ports
  - `--name [some_name]` ... and name the container
- `$ docker run --help`
- `$ docker ps` list all running containers
- `$ docker ps -a` list all containers that have been run
- `$ docker rm [container]` clean up container
- `$ docker rm $(docker ps -a -q -f status=exited)` clean up all exited containers same thing as `$ docker container prune`
- `$ docker port [container]` see port of container
- `$ docker stop [container]` stop a detached container



## basic terminology
- **images**: The blueprints of our application which form the basis of containers. In the demo above, we used the docker pull command to download the busybox image.
- **containers**: - Created from Docker images and run the actual application. We create a container using docker run which we did using the busybox image that we downloaded. A list of running containers can be seen using the docker ps command.
- **docker daemon**: - The background service running on the host that manages building, running and distributing Docker containers. The daemon is the process that runs in the operating system which clients talk to.
- **docker client**: - The command line tool that allows the user to interact with the daemon. More generally, there can be other forms of clients too - such as Kitematic which provide a GUI to the users.
- **docker hub**: - A registry of Docker images. You can think of the registry as a directory of all available Docker images. If required, one can host their own Docker registries and can use them for pulling images.

## create docker image

Docker images can be pulled from the registry on docker-hub to run. But how to make a image oneself?

### image types
- **base-images**
- **child-images**
- **official images** officially maintained and supported by Docker (e.g. `python`, `ubuntu`, `busybox`, ...)
- **user images** created and shared by users, build on base images. (`user/image-name`)

### dockerfile

A simple text file that contains a list of commands that the docker client calls while creating an image.
Simple way to automate the image creation process. Most commands are the same as the linux commands. Yay!

#### Example Dockerfile

```
# base image
FROM python:3

# set a directory for the app
WORKDIR /usr/src/app

# copy all the files to the container
COPY . .

# install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# define the port number the container should expose
EXPOSE 5000

# run the command
CMD ["python", "./app.py"]
```

## build

With the Dockerfile we can build the image.

- `$ docker build .` build an image using a dockerfile in the current directory (careful, period at END!!)
  - ` -t lucashabersaat/[tagname]` ... and tag it
  - ` -f [path/to/Dockerfile]` build an image using a dockerfile in the given path
