# docker

## tutorial
- [https://docker-curriculum.com/](https://docker-curriculum.com/)
- https://docs.docker.com/get-started/

according to wikipedia:
> an open-source project that automates the deployment of software applications inside containers by providing an additional layer of abstraction and automation of OS-level virtualization on Linux.

Docker is a tool that allows to easily deploy an application in a container. Key is that one can package an appliation with all of its dependencies into a **standardized unit**.

## containers

Industry standard is to use VM, but they have the downside of great computational overhead spent virtualizing hardware for a guest OS.

Containers leverage the low-level mechanics of the host operating system. Most of the isolation provided at fraction of computing power.


## command list
- `$ docker images` list all images
- `$ docker run imagename` find image, load up container and exit again
- `$ docker run -it busybox sh` find image, load up container and attach to interactive console
- `$ docker run --help`
- `$ docker ps` list all running containers
- `$ docker ps -a` list all containers that have been run
- `$ docker rm container_id` clean up container
- `$ docker rm $(docker ps -a -q -f status=exited)` clean up all exited containers
