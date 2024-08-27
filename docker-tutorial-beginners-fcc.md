# Docker Tutorial for Beginners - A Full DevOps Course on How to Run Applications in Containers
by `freeCodeCamp.org`, `KodeKloud.com`

YouTube: https://www.youtube.com/watch?v=fqMOX6JJhGo&list=PLWKjhJtqVAbkzvvpY12KkfiIGso9A_Ixs&index=2

Source: -

01. Introduction
02. Docker Overview
03. Getting Started
04. Install Docker
05. Commands
06. Labs
07. Run
08. Environment Variables
09. Images
10. CMD vs ENTRYPOINT
11. Networking
12. Storage
13. Compose
14.
15.
16.
17.
18.
19.
20.

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

#### Interactive & Terminal Container
`$ docker run -it {image-name|image-id}`

#### Port Mapping
`$ docker run -p {external-port:internal-port} {image-name|image-id}`

#### Volume Mapping
`S docker run -v {external-path:internal-path} {image-name|image-id}`

#### Inspect Container
`$ docker inspect {container-name|container-id}`

#### Container Logs
`$ docker logs {container-name|container-id}`

#### Docker History
`docker history {image-name|image-id}`

### Environment Variables
`$ docker run -e ENV_VAR=value {image-name|image-id}`
Use 'docker imspect' to view environment variables set.

### Create Docker Image

* Cerate DockerFile

`$ docker build {.|Dockerfile} -t {image-name}`

### Networks

* Bridge `docker run {image-name|image-id}`
* Host   `docker run {image-name|image-id} --network=host`
* Null   `docker run {image-name|image-id} --network=none`

DNS Server: 127.0.0.11

### Storage

/var/lib/docker
  + aufs
  + containers
  + image
  + volumes

#### Volume Mounting
`$ docker volume create {data_volume}`
`$ docker run -v {data_volume}:{in-directory-path} {image-name|image-id}`

#### Bindd Mounting
`$ docker run -v {out-directory-path}:{in-directory-path} {image-name|image-id}`

#### Mount Option
`$ docker run --mount type=bind,source={out-directory-path},target={in-directory-path} {image-name|image-id}`

#### Storage Drivers

* AUFS
* ZFS
* BTRFS
* Device Mapper
* Overlay
* Overlay2
### Docker Compose

`docker-compose.yaml`

`$ docker compose build`