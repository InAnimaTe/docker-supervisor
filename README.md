## Supervisor Dockerfile


This repository contains **Dockerfile** of [Supervisor](http://supervisord.org/) for [Docker](https://www.docker.com/)'s [automated build](https://registry.hub.docker.com/u/dockerfile/supervisor/) published to the public [Docker Hub Registry](https://registry.hub.docker.com/).

This repo contains the Dockerfile for a supervisor base container for most general projects needing multi-process management inside their containers. This repo was created in response to the "dockerfile" project being deprecated and there being no official supervisor image on the public registry/library.


### Base Docker Image

* [ubuntu](https://registry.hub.docker.com/_/ubuntu/)


### Installation

1. Install [Docker](https://www.docker.com/).

2. Download [automated build](https://registry.hub.docker.com/u/inanimate/supervisor/) from public [Docker Hub Registry](https://registry.hub.docker.com/): `docker pull inanimate/supervisor`

   (alternatively, you can build an image from Dockerfile: `docker build -t="inanimate/supervisor" github.com/inanimate/supervisor`)


### Usage

    docker run -it --rm inanimate/supervisor

#### Run with custom config directory

    docker run -d -v <config-dir>:/etc/supervisor/conf.d inanimate/supervisor
