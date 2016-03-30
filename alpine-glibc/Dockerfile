FROM alpine:3.3

ENV GLIBC_VERSION 2.23-r1
ENV GLIBC_SERVER https://github.com/andyshinn/alpine-pkg-glibc/releases/download 

RUN apk --no-cache add curl

RUN curl -Ls --cacert /etc/ssl/certs/ca-certificates.crt -o /tmp/glibc.apk \
   "${GLIBC_SERVER}/${GLIBC_VERSION}/glibc-${GLIBC_VERSION}.apk" \
 && curl -Ls --cacert /etc/ssl/certs/ca-certificates.crt -o /tmp/glibc-bin.apk \
   "${GLIBC_SERVER}/${GLIBC_VERSION}/glibc-bin-${GLIBC_VERSION}.apk" \
 && apk --no-cache add --allow-untrusted /tmp/glibc.apk \
 && apk --no-cache add --allow-untrusted /tmp/glibc-bin.apk \
 && rm -f /tmp/glibc*

