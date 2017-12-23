Docker-compose for Mongo db 
===========================

This project provides `docker-compose.yml`.

You can run mongo db as docker container.

This container use docker volume to store database data.
Even if you remove container, db data will be kept in docker volume.

It exposes `27017` port.

If you need to change the port, please create `docker-compose.override.yml`.

**Example) docker-compose.override.yml**

```
version: "3"

services:
  mongo:
    ports:
      - "<PORT>:27017"
```

## How to run

```
$ docker-compose up -d
```

## How to down docker

```
$ docker-compose down
```

* If you want to clear db data, add `-v` option when you execute down command.

```
$ docker-compose down -v
```
