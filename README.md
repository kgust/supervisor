## Kevin's Supervisor Base Docker Container

This repository contains **Dockerfile** of [Supervisor](http://supervisord.org/) for [Docker](https://www.docker.com/)'s [automated build](https://registry.hub.docker.com/u/kgust/supervisor/) published to the public [Docker Hub Registry](https://registry.hub.docker.com/).

### Base Docker Image

* [debian:jessie](https://registry.hub.docker.com/_/debian/)

### Installation

1. Install [Docker](https://www.docker.com/).

2. Download [automated build](https://registry.hub.docker.com/u/kgust/supervisor/) from public [Docker Hub Registry](https://registry.hub.docker.com/): `docker pull kgust/supervisor`

   (alternatively, you can build an image from Dockerfile: `docker build -t="kgust/supervisor" github.com/kgust/supervisor`)


### Usage

    docker run -it --rm kgust/supervisor

#### Run with custom config directory

    docker run -d -v <config-dir>:/etc/supervisor/conf.d kgust/supervisor
