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

## 1.5

Done.

## 1.6

Commands

```
docker run -it devopsdockeruh/pull_exercise
Give me the password: basics
```

Message:

"This is the secret message"

## 1.7

Commands

```
docker build . -t "web-server"
docker run web-server

```

[Link to Dockerfile](1.7/Dockerfile)

## 1.8

Commands

```
docker build . -t "curler"
docker run -it curler

```

[Link to Dockerfile](1.8/Dockerfile)

## 1.9

Commands

```
touch text.log
docker run -v "$(pwd)/text.log:/usr/src/app/text.log" devopsdockeruh/simple-web-service

```

## 1.10

Commands

```
docker run --rm -p 5000:8080 devopsdockeruh/simple-web-service server

```

## 1.11

Dockerfile contents

```

FROM openjdk:8

EXPOSE 8080

COPY . /usr/src/myapp

WORKDIR /usr/src/myapp

RUN ./mvnw package

CMD java -jar ./target/docker-example-1.1.3.jar

```

Commands:

```
docker build . -t "spring-project"
docker run -d --rm -p 5000:8080 spring-project
```
