# Dockers based on Alpine Linux

`docker pull` | Latest | Total size | Delivers | From | Dependencies
 ---- |:---:|:---:|:---:|:---:| ---
`terisco/alpine-glibc:3.6` | 3.6 | 12Mb | base OS | `alpine:3.6` | [`glibc-2.26-r0`][glibc-2.26-r0]
`terisco/alpine-glibc-jre:8` | 8 | 89Mb | Java runtime | `terisco/alpine-glibc:3.6` | `openjdk8-jre` via `apk`

Java dockers are delivered with [`glibc-2.26-r0`][glibc-2.26-r0].

[glibc-2.26-r0]: https://github.com/sgerrand/alpine-pkg-glibc/releases/tag/2.26-r0
