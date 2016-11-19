FROM alpine:latest
MAINTAINER MsWebmaster

WORKDIR /src
VOLUME /src
COPY startup.sh /startup.sh
RUN chmod 755 /startup.sh

RUN apk add --update mysql mysql-client && rm -f /var/cache/apk/*
COPY my.cnf /etc/mysql/my.cnf

EXPOSE 3306
CMD ["/startup.sh"]
