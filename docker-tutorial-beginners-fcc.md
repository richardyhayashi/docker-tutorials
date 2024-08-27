# Docker Tutorial for Beginners - A Full DevOps Course on How to Run Applications in Containers
by `freeCodeCamp.org`, `KodeKloud.com`

YouTube: https://www.youtube.com/watch?v=fqMOX6JJhGo&list=PLWKjhJtqVAbkzvvpY12KkfiIGso9A_Ixs&index=2

Source: -

01. Introduction
02. Docker Overview
03. Getting Started
04. Install Docker
05. Commands
06.
07.
08.
09.
10.
11.
12.
13.
14.
15.

## Notes

### Check Docker Version

`$ sudo docker version`

### Test Docker

***Does not work***
`$ docker run docker/whaleday cowsay boo`

### Commands

#### Start Container
`$ docker run {image-name}`
`$ docker run ubuntu sleep 5`

##### Detached Mode
`$ docker run -d {image-name}`

#### List Containers
`$ docker ps [-a]`

#### Stop a Container
`$ docker stop {container-name|container-id}`

#### Remove a Container
`$ docker rm {continer-name|container-id}`

#### List Images
`$ docker images`

#### Remove Images
`$ rmi {image-name|image-id}`

#### Download an Image
`$ docker pull {image-name}`

#### Execute Command in Container
`$ docker exec {container-name|container-id} {command}`

#### Attach to Running Continer
`$ docker attach {container-name|container-id}`

