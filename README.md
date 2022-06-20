# docker-projects

# Install Docker for Linux:

* Red Hat:
- `sudo yum install -y docker`
- `sudo service docker start`
- `sudo usermod -G docker $(whoami)`
- Restart operating system.
- Try: `docker` and `docker container ls`

* Ubuntu:
- Download the docker install script: `wget -qO- https://get.docker.com/ | sh`
- `sudo usermod -aG docker $(whoami)`
- Restart operating system.
- Try: `docker` and `docker contaienr ls`


* Help on creating containers 

`docker create --help `


# -- Run a Ubuntu Container and a Container Shell --

In this video, we created our first Docker container, and ran a shell within it. Below are the main commands that we used.

* Search for the ubuntu image on the command line with Docker:
- `docker search ubuntu`

* Create an interactive ubuntu container, and run bash. Name it foo:
- `docker create -it --name=foo ubuntu bash.`

* Start the created container:
- `docker start foo`

* Then attach to the container’s shell:
- `docker attach foo`

* List out running containers:
- `docker container ls`
* List out containers (whether or not they’re running)
- `docker container ls -a`

![image](https://user-images.githubusercontent.com/71001536/174623832-9e22162f-807e-43bb-b5e3-d2f9502994c7.png)

* Containers can be created, run, started and attached to with one step using `docker run.` We should also remove containers when we finish using them. Below are the main commands we went over:

* Create, start, run, and attach to a container in one step:
- `docker run --name=bar -it ubuntu bash`

* Stop a container:
- `docker stop foo`
* Remove a container:
- `docker rm foo`
* Force remove a container (stop and remove in one step):
- `docker rm -f foo`

