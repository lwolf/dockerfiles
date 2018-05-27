FROM node:7.2-alpine

MAINTAINER Sergey Nuzhdin <ipaq.lw@gmail.com>

RUN apk update \
    && apk add ca-certificates \
    && update-ca-certificates \
    && apk add openssl \
    && rm /var/cache/apk/*

ENV VERSION=0.17.9
ENV DATA_DIR="/data"

RUN npm install -g yarn@$VERSION

RUN mkdir $DATA_DIR

WORKDIR $DATA_DIR

VOLUME $DATA_DIR

ENTRYPOINT ["/bin/sh"]
