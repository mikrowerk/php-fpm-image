FROM busybox:latest
LABEL maintainer="Guenther Froestl <gfr@gammadata.de>"

COPY ./www/html  /var/www/html

#keep container running

CMD exec /bin/sh -c "trap : TERM INT; sleep infinity & wait"