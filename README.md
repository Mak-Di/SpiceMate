## DockerSpiceLxde

This repository contains **Dockerfile** of [Ubuntu Desktop (Mate)](http://ubuntu-mate.org/) for [Docker](https://www.docker.com/)'s


### Base Docker Image

* [ubuntu:14.04](https://registry.hub.docker.com/_/ubuntu/)


### Installation

1. Install [Docker](https://www.docker.com/).

2. Download [automated build](https://registry.hub.docker.com/u/gauthierc/spicemate/) from public [Docker Hub Registry](https://registry.hub.docker.com/): `docker pull gauthierc/spicemate`

   (alternatively, you can build an image from Dockerfile: `docker build -t="gauthierc/spicemate" github.com/gauthierc/SpiceMate`)


### Usage


	docker run -p 5900:5900 gauthierc/spicemate

If you local user is 'myusername' and your uid is '1000' and you want map your /home/myusername in Docker:

	docker run -p 5900:5900 -e SPICE_USER=myusername -e SPICE_UID=1000 -v /home/myusername:/home/myusername gauthierc/spicemate

Connect via Spice client 'spicec -h localhost -p 5900 -w password'

