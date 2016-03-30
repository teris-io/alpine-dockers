# Dockers based on Alpine Linux

`docker pull` | Latest | Total size | Delivers | From | Dependencies
 ---- |:---:|:---:|:---:|:---:| ---
`ventu/alpine-glibc` | 3.3 | 13Mb | base OS | `alpine:3.3` | [`glibc-2.23-r1`][glibc-2.23-r1]
`ventu/openjdk-jre` | 8 & 7 | 123Mb | Java runtime | `ventu/alpine-glibc:3.3` | `openjdk8-jre` via `apk`
`ventu/rabbitmq` | 3.6.1 | 44Mb | RabbitMQ server | `alpine:3.3` | `rabbitmq-3.6.1`, `erlang-18.1-r5` via `apk` 
`ventu/redis` | 3.0.5 | 6Mb | Redis server | `alpine:3.3` | `redis-3.0.5-r1` via `apk` 
`ventu/orientdb` | 2.1.5 | 163Mb | OrientDB graph DB | `ventu/opendjdk8-jre` | `orientdb-2.1.5`

Java dockers are delivered with [`glibc-2.23-r1`][glibc-2.23-r1].

[glibc-2.23-r1]: https://github.com/andyshinn/alpine-pkg-glibc/releases/tag/2.23-r1
