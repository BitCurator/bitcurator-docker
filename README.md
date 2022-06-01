![Logo](https://github.com/BitCurator/bitcurator.github.io/blob/main/logos/BitCurator-Basic-400px.png)

# bitcurator-docker

[![GitHub issues](https://img.shields.io/github/issues/bitcurator/bitcurator-docker.svg)](https://github.com/bitcurator/bitcurator-docker/issues)
[![GitHub forks](https://img.shields.io/github/forks/bitcurator/bitcurator-docker.svg)](https://github.com/bitcurator/bitcurator-docker/network)
[![Twitter Follow](https://img.shields.io/twitter/follow/bitcurator.svg?style=social&label=Follow)](https://twitter.com/bitcurator)

## Description:

This repository contains the source files for the docker that uses the BitCurator CLI to generate an addon installation of the toolset. Since Ubuntu Focal (20.04) is still in LTS, this docker is built using that image. The Jammy (22.04) version is not yet supported, as SaltStack does not have a 22.04-supported release, and as such there are a few 'Macgyver-isms' to get it to work properly. Once SaltStack supports Jammy, this will be updated.

## Usage:

First, this docker supports X11 forwarding. If using the ```docker-compose.yaml``` file below, modify it accordingly and run:

```sudo docker-compose up -d``` from the directory containing the compose file.

Once the docker is up, if you did not modify the IP/Port mappings below, run the following:

```ssh -X bcadmin@localhost -p 33``` or ```ssh -X bcadmin@172.22.0.3 -p 33``` with the password of ```bcadmin```

This compose file has port host-port 33 mapped to image-port 22 to avoid conflicts with any SSH server/service running on host-port 22.

**Acknowledgement:**

Developed for the BitCurator community by @digitalsleuth (https://hub.docker.com/u/digitalsleuth)

## Development Team and Support

The BitCurator environment is a product of the BitCurator team housed at the School of Information and Library Science at the University of North Carolina at Chapel Hill. Funding between 2011 and 2014 was provided by the Andrew W. Mellon Foundation.

Ongoing support for the BitCurator environment is managed by the BitCurator Consortium. Find out more at:

http://www.bitcuratorconsortium.net/
