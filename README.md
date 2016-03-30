# Dockers based on Alpine Linux

### Alpine Linux with glibc

`latest`, `3.3` built on `alpine:3.3`, [`glibc-2.23-r1`][glibc-2.23-r1]

    docker pull ventu/alpine-glibc

### OpenJDK JRE (with glibc)

`latest`, `8` built on `ventu/alpine-glibc:3.3`

    docker pull ventu/openjdk-jre

### RabbitMQ

`latest`, `3.6.1` built on `alpine:3.3`, `erlang-18.1-r5`, `rabbitmq-3.6.1`

    docker pull ventu/rabbitmq

### Redis

`latest`, `3.0.5` built on `alpine:3.3`, `redis-3.0.5-r1`

    docker pull ventu/redis

### OrientDB

`latest`, `2.1.5` build on `ventu/openjdk-jre:8`, `orientdb-2.1.5`

    docker pull ventu/orientdb



[glibc-2.23-r1]: https://github.com/andyshinn/alpine-pkg-glibc/releases/tag/2.23-r1
