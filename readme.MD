## Requirements
- Docker Engine

## Docker Instructions 
- docker build -t hellojs: latest . -> Create an image
- docker login
- docker tag webserver:v1 mn519019/webserver:v1 -> update a tag 
- docker run -d -p 80:80 --name web mn519019/webserver:v1 -> Run a docker container using webserver image -> verify whether the container is running fine
- docker push mn519019/webserver:v1

## Verfication 
- $docker ps 
```
CONTAINER ID   IMAGE              COMMAND                  CREATED         STATUS        PORTS                                       NAMES
90f0b4440315   mn519019/hellojs   "docker-entrypoint.s…"   2 seconds ago   Up 1 second   0.0.0.0:8080->8080/tcp, :::8080->8080/tcp   web
```
- $ curl localhost:8080 
```
Container hostname: 90f0b4440315
```