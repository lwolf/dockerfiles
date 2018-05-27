FROM alpine:3.4

MAINTAINER Sergey Nuzhdin <ipaq.lw@gmail.com>

RUN apk add --update curl && \
    rm -rf /var/cache/apk/*

ADD run.sh /opt/run.sh

CMD ["sh", "/opt/run.sh"]
