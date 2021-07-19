# Part1 Answers:

## 1.1

```
$ docker ps -a

CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS                      PORTS               NAMES
88994af0596c        nginx               "nginx -g 'daemon of…"   37 seconds ago      Exited (0) 14 seconds ago                       lucid_jackson
e02aa8c921a1        nginx               "nginx -g 'daemon of…"   39 seconds ago      Up 38 seconds               80/tcp              heuristic_northcutt
98739885a36c        nginx               "nginx -g 'daemon of…"   48 seconds ago      Exited (0) 14 seconds ago                       hopeful_euler
```

## 1.2

### `docker images`

```
$ docker images

REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
```

### `docker ps -a`

```
$ docker ps -a

CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES            SIZE
```

## 1.3

Commands:

```
docker run -it devopsdockeruh/simple-web-service:ubuntu
docker exec -it de1c8e6712ad bash
tail -f ./text.log
```

Result:

```
Secret message is: 'You can find the source code here: https://github.com/docker-hy'
```

## 1.4

Command to run a ubuntu container:

```
docker run -it ubuntu
```

Install curl:

```
apt-get update; apt-get install curl
```

Run script:

```
sh -c 'echo "Input website:"; read website; echo "Searching.."; sleep 1; curl http://$website;'
```