FROM alpine:latest
MAINTAINER MsWebmaster

WORKDIR /app
VOLUME /app

COPY ./startup.sh /

RUN chmod +x /startup.sh \
&& apk --update add mysql mysql-client bash \
&& rm -rf /var/cache/apk/*

COPY my.cnf /etc/mysql/my.cnf

EXPOSE 3306

ENTRYPOINT [ "/startup.sh" ]
CMD [ "mysqld", "--user=root" ]
