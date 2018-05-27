FROM alpine:3.4

MAINTAINER Sergey Nuzhdin <ipaq.lw@gmail.com>

RUN apk add --update ca-certificates \
    && apk add --update -t deps curl \
    && apk add --update python-dev curl libxml2-dev \
                        libxslt-dev libffi-dev gcc musl-dev \
                        libgcc openssl-dev \
    && curl https://bootstrap.pypa.io/get-pip.py | python \
    && apk del --purge deps \
    && rm /var/cache/apk/*

RUN pip install scrapy

ENTRYPOINT ["/usr/bin/scrapy"]
