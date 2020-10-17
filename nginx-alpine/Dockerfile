FROM nginx:1.19-alpine
LABEL maintainer="Guenther Froestl <gfr@gammadata.de>"

RUN apk add iputils drill nano wget curl

COPY fpm-site.conf  /etc/nginx/conf.d/default.conf

