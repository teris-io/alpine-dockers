FROM ventu/openjdk-jre:8

MAINTAINER info@ventu.io

ENV ORIENTDB_VERSION 2.1.5
ENV ORIENTDB_DOWNLOAD_MD5 05ddff3dc606f602d00c00ad365a66b1
ENV ORIENTDB_DOWNLOAD_SHA1 75ff03e5a5cfdfa59afa42725bfae4eb0dc9a97e

RUN apk --update --no-cache add tar \
  && mkdir /orientdb \
  && curl -L  "http://central.maven.org/maven2/com/orientechnologies/orientdb-community/$ORIENTDB_VERSION/orientdb-community-$ORIENTDB_VERSION.tar.gz" -o orientdb-community-$ORIENTDB_VERSION.tar.gz \
  && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c - \
  && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c - \
  && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1\
  && rm orientdb-community-$ORIENTDB_VERSION.tar.gz \
  && rm -rf /orientdb/databases/*

ENV PATH /orientdb/bin:$PATH

VOLUME ["/orientdb/backup", "/orientdb/databases", "/orientdb/config"]

WORKDIR /orientdb

#OrientDb binary
EXPOSE 2424

#OrientDb http
EXPOSE 2480

# Default command start the server
CMD ["server.sh"]