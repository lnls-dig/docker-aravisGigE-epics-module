Docker image with the aravisGigE EPICS Module installed 
==================================================================

This repository contains a Dockerfile used to create a Docker image with the
[aravisGigE EPICS Module](https://github.com/areaDetector/aravisGigE).

This module is used to build IOCs that communicate with aravis-genicam compatible cameras.

## Running the Docker Container

The simples way to run the container is to run:

    docker run --rm -it --net host lnlsdig/aravisgige-epics-module

## Creating a Persistent Container

If you want to create a persistent container with the module, you can run a
command similar to:

    docker run -it --net host --restart always --name CONTAINER_NAME lnlsdig/aravisgige-epics-module

where `CONTAINER_NAME` is the name given to the container.

## Building the Image Manually

To build the image locally without downloading it from Docker Hub, clone the
repository and run the `docker build` command:

    git clone https://github.com/lnls-dig/docker-aravisGigE-epics-module
    docker build -t lnlsdig/aravisgige-epics-module docker-aravisGigE-epics-module
