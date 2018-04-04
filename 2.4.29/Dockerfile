FROM alpine:3.7
MAINTAINER WPLib Team <team@wplib.org>

RUN apk add --no-cache bash apache2=2.4.29-r1 apache2-proxy=2.4.29-r1 apache2-ssl=2.4.29-r1 && \
	mkdir -p /run/apache2

COPY container.json /etc/container.json
COPY files /

EXPOSE 80 443

CMD ["/usr/sbin/httpd", "-DFOREGROUND"]
