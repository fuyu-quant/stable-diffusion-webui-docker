# stable-diffusion-webui-docker
stable diffusionをgradioで起動する

## Contents
* [Setting](#setting)
* [Basic docker operations](#basic-docker-operations)
    * [Basic docker commands](#basic-docker-commands)
    * [How to run the Dockerfile](#how-to-run-the-dockerfile)
* [stable-diffusion-webui](#stable-diffusion-webui)



## Setting
Install nvidia-install-docker in the base environment as follows
nvidia-container-runtime
```bash
# CentOS
yum install nvidia-container-runtime
# Ubuntu
apt-get install nvidia-container-runtime
```
For more information, please check the following links
https://github.com/NVIDIA/nvidia-container-runtime



## Basic docker operations
### Basic docker commands
```Dockerfile
# Enter the container
docker-compose exec Docker-service-name bash

# Docker image list
docker images

# Remove docker image
dokcer rmi Image-name

# Check active containers
docker ps -a

# Docker network list
docker network ls

# Details of any docker network
docker network inspect Network-name

# Delete unused container data
docker system prune

# Container to container http communication
# container name : Container name for communication destination
# port : Open ports of the container to which you are communicating
curl http://[container name]:[port]/
# example
curl http://fastapi:8040/
```


### How to run the Dockerfile
How to start a dockerfile using Docker compose
```bash
# Start container
bash docker.sh up

# Rebuild the docker image and start container
bash docker.sh force

# Stop container
bash docker.sh down

# Stop the container and delete the image
bash docker.sh rm 
```


## stable-diffusion-webui
* http://localhost:7860

