![Logo](https://github.com/BitCurator/bitcurator.github.io/blob/main/logos/BitCurator-Basic-400px.png)

# bitcurator-docker

[![GitHub issues](https://img.shields.io/github/issues/bitcurator/bitcurator-docker.svg)](https://github.com/bitcurator/bitcurator-docker/issues)
[![GitHub forks](https://img.shields.io/github/forks/bitcurator/bitcurator-docker.svg)](https://github.com/bitcurator/bitcurator-docker/network)

## Description

This repository contains the source files for a docker container that uses the BitCurator CLI to generate an addon installation of the toolset. Both Jammy (22.04) and Focal (20.04) LTS versions of Ubuntu are supported by the CLI. However, the files in this repository are configured by default to build images using 22.04 with SaltStack release 3005. If you wish to build an image using 20.04, you will need to modify them.

## Images

[Download the latest release from our Docker Hub](https://hub.docker.com/r/bitcurator/bitcurator).

## Usage

First, this docker supports X11 forwarding. If using the ```docker-compose.yaml``` file below, modify it as required and run:

```sudo docker compose up -d``` from the directory containing the compose file.

Once the docker is up, if you did not modify the IP/Port mappings below, run the following:

```ssh -X bcadmin@localhost -p 33``` or ```ssh -X bcadmin@172.22.0.3 -p 33``` with the password of ```bcadmin```

This compose file has port host-port 33 mapped to image-port 22 to avoid conflicts with any SSH server/service running on host-port 22.

## Acknowledgement

Developed for the BitCurator community by [@digitalsleuth](https://github.com/digitalsleuth).

## Development Team and Support

The BitCurator environment is a product of the BitCurator team housed at the School of Information and Library Science at the University of North Carolina at Chapel Hill. Funding between 2011 and 2014 was provided by the Andrew W. Mellon Foundation.

Community support is managed by the BitCurator Consortium. Find out more at:

http://www.bitcuratorconsortium.org/

