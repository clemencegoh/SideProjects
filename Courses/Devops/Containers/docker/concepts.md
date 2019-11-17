# What is docker?
* Platform as a Service (PaaS)
* Allows the running of apps which have been *dockerized* such that all the env variables have been encapulated within the container itself


# What do I need to know?
* How to use docker
    * Run images (attached and detached processes)
    * View images that have been run/are running
        * `docker ps -a`
    * Running different versions of the images
    * Input mapping into the docker container (Does not accept inputs by default)
        * Run with `docker run -it <application>`
        * This denotes interactive terminal flag, which attaches an interactive terminal on the current input
* How to Dockerize an app
* How to interact with App on docker once deployed
    * Docker container is assigned an IP
        * Internal only, can only be accessed within the docker host.
    * Note that to access it outside of the Docker host, docker app within the container must have been mapped to a free port on the docker host.
        * Example: `docker run -p 80:5000 <application>`
            * This maps port 80 on the external host IP to port 5000 on the docker internal application 
            * Another example: SQL `docker run -p 3306:3306 mysql`
                * Route externalIP:3306 to internalIP:3306
            * Similarly, `docker run -p 8306:3306 mysql` routes external 8306 into internal 3306
        * **NOTE**: Obviously, cannot map to a port more than once


## Persistent Data in docker container
* Since the container deletes all data once it has been stopped, persistent data cannot be stored.
* Alternatively, map a directory outside the container to one inside:
    * Use `docker run -v /opt/datadir:/var/lib/mysql mysql`
        * In this case, the `/opt/datadir` exists outside the container, mapped to `/var/lib/mysql/` within the container


## Getting details of a docker config
* use `docker inspect <application>`
    * returns all config details in a json format


## How to build an image:
![creating docker image](images/creating_docker_image.jpg)
![what is in a dockerfile](images/dockerfile_contents.jpg)
* Use `docker build Dockerfile -t <application>` to build
    * this uses cache such that it does not need to reinstall dependencies


## Stopped:
* https://www.youtube.com/watch?v=fqMOX6JJhGo
* 58:48