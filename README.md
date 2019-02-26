# Multiparty Meeting => MM
MM stand as a shortcut for multiparty-meeting.

This is the container, or a "dockerized" version of the [multiparty meeting](https://github.com/havfo/multiparty-meeting),
and like MM is shortcut, this container is a simillar shortcut that saves time.
:)

## Run it in few easy step.
1. git clone this code to your docker machine.
2. copy your cert in `certs/cert.pem` and `certs/privkey.pem`
2. configure your app side configs
   e.g. Set TURN server and credential in `configs/app/config.js`
3. configure your server side configs
   e.g. Set TURN server and credential in `configs/server/config.js`

## Run:
There is two ways
1. simple use `docker run` command
```
./run.sh
```

2. or with `docker-compose` 
/ [install docker compose](https://docs.docker.com/compose/install/) /
```
  docker-compose up --detach
```
## Rebuild

If you change app-config.js or or something in .env then you have to rebuild the image.
```
  docker-compose up --build --detach
```

## Docker networking
Container works in "host" network mode, because birdge mode has the following issue

[Docker - Docker hangs when attempting to bind a large number of ports] (https://success.docker.com/article/docker-compose-and-docker-run-hang-when-binding-a-large-port-range)


## Further Informations 
Read more about configs and settings in [multiparty meeting](https://github.com/havfo/multiparty-meeting) README.
