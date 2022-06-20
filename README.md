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

